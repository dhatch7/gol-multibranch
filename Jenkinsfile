pipeline {
    agent { label 'myp2' }
     triggers {
        cron('59 23 * * *')
    }
    stages {
        stage('SCM') {
            steps {
                git branch: 'qa', url: 'https://github.com/dhatch7/gol-multibranch.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
