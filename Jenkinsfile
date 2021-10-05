node('walmart-node')
{
 def mavenhome = tool name: "maven3.8.2"
     
 stage('checkoutCode'){
 git branch: 'development', credentialsId: '376e97aa-0091-4538-9818-9f361484f2ae', 
 url: 'https://github.com/snehaprudhvi/maven-web-application.git'    
 }
 stage('build'){
 sh "${mavenhome}/bin/mvn clean package"
 }
 /*
 stage('Executesonarqubereport'){
 sh "${mavenhome}/bin/mvn clean sonar:sonar" 
 }
stage('uploadartifactintonexusrepository'){
sh "${mavenhome}/bin/mvn clean deploy"
}
stage('deploytomcatintotomcatapplicationserver')
   sshagent(['9827bfea-95b9-4315-9d74-051ca48e7978']) {
    sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@52.53.171.148:/opt/apache-tomcat-9.0.53/webapps"
}
  stage('send emailnotification'){
      mail bcc: 'snehaprudhvi12@gmail.com', body: '''build over 


regards
snehaprudhvi''', cc: 'snehaprudhvi12@gmail.com', from: '', replyTo: '', subject: 'build over', to: 'snehaprudhvi12@gmail.com'
  }  
  */
}
