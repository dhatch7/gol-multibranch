pipeline {
    agent { label 'MASTER' }
    stages {
        stage('SCM') {
            steps {
               git branch: 'release', url: 'https://github.com/dhatch7/gol-multibranch.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
