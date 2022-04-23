pipeline {
    agent any

    
    stages {
        stage('gitclone') {
            steps {
                
                git 'https://github.com/suvidhakudumula/example-tomcat-war.git'

               
            }

          
        }
        stage('build') {
            steps {
                sh "mvn clean install"
                sh "mvn package"
            }
        }
        stage('deploy to tomcat') {
            steps {
                sh "cp /var/lib/jenkins/workspace/java_pipeline/target/SimpleTomcatWebApp.war  /usr/share/tomcat/webapps"
            }
        }
    }
}
