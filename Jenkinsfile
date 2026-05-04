pipeline {
    agent any

    stages {
        stage('Deploy to S3') {
            steps {
                sh '''
                /opt/homebrew/bin/aws s3 sync . s3://sufal-practice-static-page \
                --exclude ".git/*" \
                --exclude "Jenkinsfile" \
                --delete
                '''
            }
        }
    }
}