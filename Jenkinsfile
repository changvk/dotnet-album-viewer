pipeline {  
    agent any
    triggers {
    cron('H/2 * * * *')
    }
    stages {
        stage('Build') {
            steps {
            bat 'C:/Jenkins/test.bat'
                }
            }
         stage('Test') {
            steps {
            bat 'C:/Jenkins/test.bat'
                }
            }
        stage('Package') {
            steps {
            bat 'C:/Jenkins/test.bat'
                }
            }
        stage('Deploy') {
            steps {
            bat 'C:/Jenkinstest.bat'
                }
            }
 
       post {
       failure {mail to: 'cvkai90@gmail.com',
       subject: "Pipeline has failed: ${currentBuild.fullDisplayName}",
       body: "Error in ${env.BUILD_URL}"
       }
}
