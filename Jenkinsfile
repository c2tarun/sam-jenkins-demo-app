pipeline {
    agent any

    stages {
        stage('beta') {
            environment {
                STACK_NAME = 'sam-app-beta-stage'
                S3_BUCKET = 'sam-jenkins-demo-us-west-2'
            }
            steps {
                withAWS(credentials: 'sam-jenkins-demo-credentials', region: 'us-west-2') {
                  dir ("hello-world") {
                      sh 'pwd'
                      sh 'ls'
                  }
                }

            }
        }
    }
}
