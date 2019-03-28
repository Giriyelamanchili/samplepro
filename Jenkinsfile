pipeline {
  agent any
  
    emailext body: 'testing for the email notifications', subject: 'jenkins pipeline email notification', to: 'ygiriesh@gmail.com'  
    stages {
        
      stage('Build') {
            steps {
                echo 'Building'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
    post {
        always {
          step([$class: 'Mailer',
            notifyEveryUnstableBuild: true,
            recipients: "ygiriesh@example.com",
            sendToIndividuals: true])
        }
      }
    }
  

