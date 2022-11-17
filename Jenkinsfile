pipeline {
  agent any
  stages {
    stage('Build'){
      steps {
        echo "Build"
      }
    }
  }

  stages {
    stage('Test'){
      steps {
        echo "Test"     
      }          
    }
  }
  stages {
    stage('Integration Test'){
      steps {
        echo "Integration Test"     
      }          
    }
  } post {
      always {
        echo 'Im awesome. I run always'
      }
      success {
        echo 'I run when you '
      }
      failure {
        echo 'I run when you failure '
      }
  }

}
