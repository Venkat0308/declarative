def COLOR_MAP = [...]
def getBuildUser(){...}
pipeline {
         agent any
         stages {
                  stage ("shell execute")
          {
                   steps
                   { 
                         sh 'echo $JAVA_HOME'
                   }
          } 
                  stage ("slack")
          {
                   steps
                   { 
                        slackSend channel: '#venkat',
                color: COLOR_MAP[currentBuild.currentResult],
                message: "*${currentBuild.currentResult}:* Job ${env.JOB_NAME} build ${env.BUILD_NUMBER} by ${BUILD_USER}\n More info at: ${env.BUILD_URL}"
                   }
          } 
         
        }
}
