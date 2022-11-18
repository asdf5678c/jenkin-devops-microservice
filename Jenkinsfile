pipeline {
    agent { docker { image 'node:19.1.0'} }

    stages {
        stage('Build') {
            steps {
                sh 'node --version'
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
        changed {
            echo 'cc change'
        }
    }
}
