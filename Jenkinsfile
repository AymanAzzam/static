pipeline {
    agent any 
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(credentials:'aws-static',region:'us-east-1') {
                    s3Upload(file:'index.html', bucket:'udacity-project3-jenkins', path:'index.html')
                }
            }
        }
    }
}
