Pipeline{
         agent any 
      stages {
           stage('checkout'){
                steps{
                    git 'https://github.com/siddhipande3/GRRAS03.git'
                  }
              } 
            stage(build){
                   steps{    sh 'mvn install'
          }
         }
            stage(deploy){
                steps{
                     sh cp target/GRRAS03.war/home/siddhi/Downloads/apache-tomcat-9.0.93/webapps
                }
              }
           }
        }

