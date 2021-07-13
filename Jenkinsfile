pipeline {
    agent { label 'myp1' }
     triggers {
        cron('H * * * 1-5')
    }
    stages {
        stage('SCM') {
            steps {
                git branch: 'developer', url: 'https://github.com/dhatch7/gol-multibranch.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
