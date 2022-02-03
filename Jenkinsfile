pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
            
        }
        stage('Deliver') {
            steps {
                sh '/var/lib/jenkins/workspace/jenkins_project/scripts/deliver.sh'
            }
        }
    }
}
