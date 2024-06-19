pipeline {  
    agent any
    triggers {
        cron('H/2 * * * *')
    }
    stages {
        stage('Parallel') {
            steps {
                parallel(
                "Task 1" : {
                    echo 'this is task 1.'
                }
                     "Task 2" : {
                    echo 'this is task 2.'
                }
                    )
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
                bat 'C:/Jenkins/test.bat'
            }
        }
    }
    post {
        failure {
            mail to: 'cvkai90@gmail.com',
            subject: "Pipeline has failed: ${currentBuild.fullDisplayName}",
            body: "Error in ${env.BUILD_URL}"
        }
    }
}
