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
                //sh 'ssh -o StrictHostKeyChecking=no user@172.31.116.110 uname -a'
                sh 'scp -r -o StrictHostKeyChecking=no public/javascripts/* user@172.31.116.110:/home/user/stuff/.'
            }
        }  
     
    }
        
    }
}
