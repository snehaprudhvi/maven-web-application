node('walmart-node'){
    
    def mavenhome = tool name: "maven3.8.2"
    
    stage('CheckoutCode'){
      git branch: 'development', credentialsId: '31fc31cd-8989-46ba-8599-b8a9c9ed0ac1',
      url: 'https://github.com/snehaprudhvi/maven-web-application.git'  
        }
    stage('Build'){
        sh "${mavenhome}/bin/mvn clean package"
        }
    stage('Execute Sonar Cube Report'){
        sh "${mavenhome}/bin/mvn clean sonar:sonar"
        }
    stage('Upload Artifact into Nexus Repository'){
        sh "${mavenhome}/bin/mvn clean deploy"
        }
}
    /*
    stage("Deploy Application in Tomcat Server"){
        sshagent(['fb8db3f3-71b4-41fd-887e-871d96158a75']) {
        sh "scp -o  StrictHostKeyChecking=no target/maven-web-application.war ec2-user@54.193.242.206:/opt/apache-tomcat-9.0.53/webapps"
        }
        }
    */
