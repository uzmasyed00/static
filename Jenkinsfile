pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'echo "HelloWorld"'
                sh '''
                    echo "Multiline steps work too"
                    ls -lah
                '''
            }
        }
    }
}