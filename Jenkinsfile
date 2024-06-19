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
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
        
        post {
           failure {mail to: 'cvkai90@gmail.com',
           subject: "Pipeline has failed: ${currentBuild.fullDisplayName}",
           body: "Error in ${env.BUILD_URL}"
                   }
      }
    }
}
