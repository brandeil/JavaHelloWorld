pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'echo "Deploy stage"'   
            }
        }
        
        stage('Post') {
            always {
                echo 'This will always run'
            }
            success {
                echo 'successful pipeline'   
            }
            failure {
                echo 'failed pipeline'
            }
        }
    }
}
