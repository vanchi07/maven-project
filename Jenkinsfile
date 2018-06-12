pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package-pipeline-code'
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