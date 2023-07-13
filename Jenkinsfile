pipeline {
    agent any
    stages{
        stage("Create a docker container "){
            steps{
                
            sh '''
             mkdir /dev1
             cp -vrf * /dev1
            if docker ps | grep dev1
            then 
              echo 'already running'
            else
              if docker ps | grep dev1
               then 
                docker rm -f dev1
              fi
              else
                docker run -itd -p 81:80 -v /dev1:/usr/local/apache2/htdocs/ --name dev1 httpd
            fi
            '''
                 
            }
        }
        
    }
}
