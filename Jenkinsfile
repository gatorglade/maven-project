pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                command 'mvn clean package'
            }
            post{
                success{
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}