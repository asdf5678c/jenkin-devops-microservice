pipeline {
    //agent { docker { image 'node:19.1.0'} }
    agent any
   
    environment {
       dockerHOME = tool 'myDocker'
       mavenHOME = tool 'myMaven'
       PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
    }


    stages {
        stage('Build') {
            steps {
                echo "$PATH"
                sh 'ls $dockerHome/bin'
                sh 'mvn --version'
                sh 'docker --version'
                echo 'Build done'
                echo "PATH - $PATH"
                echo "BUILD_NUMBER - $env.BUILD_NUMBER"
                echo "BUILD_ID - $env.BUILD_ID"
                echo "JOB_NAME - $env.JOB_NAME"
                echo "BUILD_TAG - $env.BUILD_TAG"
                echo "BUILD_URL - $env.BUILD_URL"
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
