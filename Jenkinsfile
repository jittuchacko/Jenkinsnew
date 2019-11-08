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
            steps {
                   echo 'Running selenium test'
            }
                stage ('Integration Test')
            steps {
                   echo 'Running Integration Test'
            }
             }
                 }
           
      }
   }
