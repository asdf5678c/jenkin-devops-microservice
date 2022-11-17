pipeline {
    agent { docker { image 'maven:latest'} }

    stages {
        stage('Build') {
            steps {
                sh 'mvn --version'
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
