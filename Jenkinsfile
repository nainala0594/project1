pipeline {

   agent any
   
   stages{
   
     stage('install dependencies') {
       steps {
         sh 'npm install'
       }
     }
     stage('test'){  
       steps {
         sh 'echo "testing application.."'
       }
     }
     
     stage("Deploy nodejs") {
       steps {
         sh 'echo "deploying.."'
       }
     }  
  }
}
  
