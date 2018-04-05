pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean pipeline'
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