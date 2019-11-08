pipeline {
   agent any

   stages {
      stage('Build') {
         steps {
            echo 'Building Image'
         }
      }
      stage('Test'){
         parallel {
                stage ('Selenium Web Test')
            {
            steps {
                   echo 'Running selenium test'
            }
            }
                stage ('Integration Test')
            {
            steps {
                   echo 'Running Integration Test'
            }
            }
             }
                 }
      stage('Push to Registry'){
         steps {
            echo 'Pushing Docker Image to Registry'
         }
      }
      stage ('Deploy') {
         steps {
            echo 'Pull Image from Registry and Deploy to cluster'
         }
      }
      stage ('Check status') {
         steps {
            echo 'Check Deployment status'
         }
      }
      stage ('Send Notification about status') {
      steps {
         echo 'Send Email Notification about deployment status'
      }
      }
      }
   }
