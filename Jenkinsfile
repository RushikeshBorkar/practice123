pipeline{
       agent any
              stages  {
                      stage ("stage 1"){
                             steps{

                              echo "this is 1st stage"
                            sh "yum install httpd -y"
                          
                          sh "docker run -dp -- name test 80:80 httpd"
                            sh "docker cp /root/.jenkins/workspace/to\ deploy\ index.html\ on\ container/index.html test:usr/local/apache2/htdocs"
                              sh "chmod -R 777 usr/local/apache2/htdocs/index.html"        
                            
                             }

                        
                      }


                
              }


  
}
