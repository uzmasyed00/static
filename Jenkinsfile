pipeline{
    agent any
    stages{
        stage('Upload to AWS'){
            steps{
                sh 'echo "HelloWorld"'
                withAWS(credentials:'aws-static') {
                    s3Upload(file:'index.html', bucket:'jenkins-pipeline-project3', path:'index.html')
                }
                sh '''
                    echo "Multiline steps work too"
                    ls -lah
                '''
            }
        }
    }
}