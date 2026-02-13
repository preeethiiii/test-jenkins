pipeline {
    agent any
    tools {
        maven 'Maven 3' // Must match the name in Global Tool Configuration
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '**/target/*.jar', allowEmptyArchive: true
            }
        }
    }
}
