pipeline {
    agent any 
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(profile:'default') {
                  sh '''
                  echo $AWS_ACCESS_KEY_ID
                  echo $AWS_SECRET_ACCESS_KEY
                  echo $AWS_SESSION_TOKEN
                  '''
                  s3Upload(file:'index.html',bucket: 'udacity-project3-jenkins', path: "index.html")
                }
            }
        }
    }
}
