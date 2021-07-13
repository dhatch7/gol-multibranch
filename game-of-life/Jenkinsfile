pipeline {
    agent { label 'myp1' }
     triggers {
        cron('59 23 * * *')
    }
    stages {
        stage('SCM') {
            steps {
                git 'https://github.com/dhatch7/gol-multibranch.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
