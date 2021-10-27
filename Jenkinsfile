pipeline{
    agent any
    tools{
        maven 'maven'
    }
    parameters{
        choice(name: 'tasks', choices: ['clean', 'install', 'package'], description: 'slsect the build type')
    }
    stages{
        stage('git'){
            steps{
                git 'https://github.com/nainala0594/project1.git'
            }
        }
                
        stage('build'){
            steps{
                sh 'mvn ${tasks}'
            }
            
        }        
        
        stage('deploy'){
            steps{
                sshagent(['deployer_1']) {
                   sh "scp -o StrictHostKeyChecking=no target/mahaLogin-1.0.war tomcat9@172.31.92.56:/opt/tomcat8/webapps"
                }
            }
        }
         
    }
}
  
