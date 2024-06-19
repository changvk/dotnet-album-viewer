pipeline {
    agent any
    triggers{
    cron('H/5 * * * *')
    }
    stages {
        stage('Build') {
            steps {
                bat 'c:/Jenkins/test.bat'
            }
        }
        stage('Test') {
            steps {
                bat 'c:/Jenkins/test.bat'
            }
        }
        stage('Package') {
            steps {
                bat 'c:/Jenkins/test.bat'
            }
        }
        stage('Deploy') {
            steps {
                bat 'c:/Jenkins/test.bat'
            }
        }
        stage('Production') {
            steps {
                bat 'c:/Jenkins/test.bat'
            }
        }
         stage('Final Production') {
            steps {
                bat 'c:/Jenkins/test.bat'
                cmd echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                cmd echo '%BUILD_NUMBER%'
            }
        }
    }
}
