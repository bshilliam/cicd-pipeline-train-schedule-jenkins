pipeline {
    agent any
    
       
    stages {
        stage('say hello') {
            steps {
                echo 'Hello man!' 
            }
        }
      stage('scp files') {
            steps {
                sshagent (credentials: ['user_hard']) {
                //sh 'ssh -o StrictHostKeyChecking=no user@172.31.116.110 uname -a'
                //sh 'scp -r -o StrictHostKeyChecking=no public/javascripts/* user@172.31.116.110:/home/user/stuff/.'
                sh 'rsync -anv --delete public/javascripts/ user@172.31.116.110:/home/user/stuff/'
            }
        }  
     
    }
        
    }
}
