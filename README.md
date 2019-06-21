<h1>jenkins master and slave installation Playbook</h1>

NOTE: to install jenkins directly without generating password, follow below:

executing Jenkins without security screen:
java -Djenkins.install.runSetupWizard=false -jar jenkins.war 


Creating user in Jenkins by cli:
echo 'jenkins.model.Jenkins.instance.securityRealm.createAccount("user1", "password123")' |
java -jar jenkins-cli.jar -s http://localhost/ groovy =

With creds:
echo'jenkins.model.Jenkins.instance.securityRealm.createAccount("user", "password")' | java -jar jenkins-cli.jar -auth admin:c3a5dcd6bc3f45ee8d6c9f0f5abc14c0 -s http://localhost:8080/ groovy =


java -jar jenkins-cli.jar -s "http://localhost:8080" -auth username:password who-am-i
