pipeline {  
    agent any
     parameters {         
        string(name: 'p_developer', defaultValue: 'Developer Name', description: 'The developer name')         
        string(name: 'p_greets', defaultValue: 'Give Greet', description: 'Greet')     
    }  
    stages {
        stage('Parallel') {
            steps {
                parallel(
                    "Task 1": {
                        echo 'this is task 1.'
                    },
                    "Task 2": {
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
        stage('Greet') {             
            steps {                 
                script {                     
                    def greetingMessage = "${params.p_developer}, ${params.p_greets}!"                     
                    echo greetingMessage                 
                }             
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
