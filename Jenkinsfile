Pipeline{
      agent any
     parameters {
  choice choices: ['UAT', 'QA', 'DEV'], name: 'ENVIRONMENT'
}
             stages{
                 stage( 'checkout' ){
                   steps{  
                      git 'https://github.com/siddhipande3/GRRAS03.git'
                        }
                      }
                  stage( 'build'){
                    steps{ 
                        sh 'mvn  install'
                        }
                      }
                   stage( 'Deployment' ){
                     steps{
                       script {
                     if (env.ENVIRONMENT == 'QA' ){
                       sh 'cp target/GRRAS03.war /home/siddhi/Downloads/apache-tomcat-9.0.93/webapps'
                       echo "deployment has been done on QA!"
                          }
                       else if ( env.ENVIRONMENT == 'UAT' ){
                        sh 'cp target/GRRAS03.war /home/siddhi/Downloads/apache-tomcat-9.0.93/webapps'
                          echo "deployment has been done on UAT!"
                        } }
                      } }
                   }
                  }
  
          
