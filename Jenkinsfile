pipeline {
    agent any
    
    stages {
        stage('Git clone') { 
            steps {
                git branch: 'main', url: 'https://github.com/dineshgulve/Demo-java.git'
            }
        }
        stage('Build') { 
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Deploy to tomcat') { 
            steps {
                sh 'echo "i am Deploying"'
                sh 'sudo cp "/var/lib/jenkins/workspace/MyFirstPipeline/target/my-java-app-1.0-SNAPSHOT.war" /tomcat/apache-tomcat-10.1.35/webapps/'
            }
        }
    }
}
