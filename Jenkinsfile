pipeline {
    agent any
    
       
    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello man!' 
            }
        }
      stage('Stage 2') {
            steps {
                sshagent (credentials: ['user_hard']) {
                sh 'ssh -o StrictHostKeyChecking=no 172.31.116.110 uname -a'
            }
        }  
     
    }
        
    }
}
