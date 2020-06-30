pipeline {
    agent any
    stages {
        stage('lint HTML'){
            steps {
                sh 'tidy -q -e *.html'
            }
        }
        stage('upload to AWS') {
            steps {
                withAWS(region:'us-west-2', credentials:'aws-static'){                
                        s3Upload(file:'index.html', bucket:'s3-bucket-for-jenkins', path:'')
                }
            }
        }
    }
}
