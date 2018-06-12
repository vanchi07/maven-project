pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                bat 'mvn clean package-pipeline-code'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}