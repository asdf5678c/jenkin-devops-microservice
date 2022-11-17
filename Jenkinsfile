pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build done'
            }
        }
        stage('Test') {
            steps {
                echo 'Test done'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy done'
            }
        }
    } 
    post {
        always {
            echo 'Im awesome. I run always'
        }
        success {
            echo 'aa success'
        }
        failure {
            echo 'bb failure'
        }
    }
}
