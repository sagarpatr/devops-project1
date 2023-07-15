
pipeline {
    
    agent any
    
    stages {
       stage('Pre checkout') {
            steps {
                echo "add the checkout code"
            }
        }      
        stage('Checkout') {
            steps {
                echo "add the checkout code"
            }
        }
        stage('maven build') {
            steps {
                echo "maven command addhere"
            }
        }
        stage('Artifact Publish') {
            steps {
                echo "maven test"
            }
        }  
        stage('Unit Test') {
            steps {
                echo "maven test"
            }
        }
       stage('sonar scan') {
            steps {
                echo "maven test"
            }
        }    
        stage('Blackduck scan') {
            steps {
                echo "maven test"
            }
        }            
        stage('Coverity Scan') {
            steps {
                echo "Docker build here"
            }
        }  
        stage('Docer publish') {
            steps {
                echo "docke publish"
            }
        }
        stage('helm build') {
            steps {
                echo "helm build coomand add here"
            }
        }        
        stage('helm publish') {
            steps {
                echo "helm build coomand add here"
            }
        }     
        stage('Integration Test') {
            steps {
                echo "helm build coomand add here"
            }
        }
        stage('Deploy') {
            steps {
                echo "helm build coomand add here"
            }
        }  
    }     
post {
    always {
        // Cleanup steps
        deleteDir()
    }
    success {
          // Action to be executed for the success pipeline
        echo "Pipeline succeedde"
        sendEmail("success")
    }
    failure {
        // Action to be executed for the failed pipeline
        echo "Pipeline failed"
        sendEmail("failed")
    }
}     
    
}

def sendEmail(String status) {
    emailext (
        subject: "Pipeline $status: ${env.JOB_NAME}",
        body: """<p>Pipeline $status: ${env.JOB_NAME}</p>
                 <p>Build URL: ${env.BUILD_URL}</p>""",
        to: 'pythonbismoy@gmail.com',
        attachLog: true
    )
}





    
