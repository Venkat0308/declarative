pipeline{
         agent any
         stages{
                  stage ("shell execute")
          {
                   steps
                   { 
                         sh 'echo $JAVA_HOME'
                   }
          } 
                  stage ("shell execute")
          {
                   steps
                   { 
                        slackSend color: "#439FE0", message: "Build Started: ${env.JOB_NAME} ${env.BUILD_NUMBER}"
                   }
          } 
         }
        }
