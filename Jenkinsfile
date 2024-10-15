pipeline{
    agent any
    stages{
        stage("Dev Tools Check") {
            steps {
                sh "mvn --version"
                sh "java --version"
            }
        }
        stage('Dev mvn clean') {
            agent { label 'DEV' }
            steps { 
                sh "mvn clean"
            }
        }
        stage('Dev mvn test') {
            agent { label 'DEV' }
            steps { 
                sh "mvn test"
            }
        }
    }
}