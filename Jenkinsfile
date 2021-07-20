
pipeline {
         agent any
         stages {
                  stage ("shell execute")
          {
                   steps
                   { 
                         sh 'exit 0'
                   }
          } 
                  stage ("slack")
          {
                   steps
                    catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                    sh "exit 1"
                   { 
                        slackSend channel: '#venkat',
            color: 'good',
            message: "*${currentBuild.currentResult}:* Job ${env.JOB_NAME} build ${env.BUILD_NUMBER}\n More info at: ${env.BUILD_URL}"
                   }
          } 
         
        }
}
