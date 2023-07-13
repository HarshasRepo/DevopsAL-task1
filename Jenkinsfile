pipeline {
  agent {
    sh '''
    sudo cp -vrf * /dev1
    if sudo docker ps | grep dev1
    then 
      echo 'already running'
    else
      if sudo docker ps | grep dev1
       then 
        sudo docker rm -f dev1
      fi
      else
        sudo docker run -itd -p 81:80 -v /dev1:/usr/local/apache2/htdocs/ --name dev1 httpd
    fi
    '''
  }
}
