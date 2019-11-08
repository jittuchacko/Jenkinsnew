pipeline {
   agent any

   stages {
      stage('Build') {
         steps {
            echo 'Building Image'
         }
      }
      stage('Test'){
          steps {
             parallel(
                a: {
                   echo 'How are you'
                }
                b: { 
                   echo 'Hope you are fine'
                   }
                )
                 }
          }
           
      }
   }
