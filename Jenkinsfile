pipeline {

   agent any
   
   stages{
   
     stage('install dependencies') {
       steps {
         sh 'apt npm install'
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
  
