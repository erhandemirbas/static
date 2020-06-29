pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-west-2', credentials: 'aws-static') {
                        s3Upload(file:'index.html', bucket:'s3-bucket-for-jenkins', path:'')
                }
            }
        }
    }
}
