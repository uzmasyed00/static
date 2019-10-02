pipeline{
    agent any
    stages{
        stage('Lint HTML'){
            steps{
                sh 'tidy -q -e *.html'
            }
        }
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