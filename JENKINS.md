Change password > GO JENKINS_URL/script

and run this script

// --------------
import jenkins.model.*
import hudson.security.*

def instance = Jenkins.getInstance()

// Replace with the desired username and password
def username = "Quefuemen"
def password = "12345678"

def hudsonRealm = new HudsonPrivateSecurityRealm(false)
instance.setSecurityRealm(hudsonRealm)
hudsonRealm.createAccount(username, password)
instance.save()
