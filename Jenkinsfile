pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'g++ new.cpp -o new'
      }
    }
    
    stage('Test') {
      steps {
        sh './new'
      }
    }
    
    stage('Deploy') {
      steps {
        sh 'scp new user@server:/path/to/destination'
      }
    }
  }
  
  post {
    always {
      steps {
        if (currentBuild.result == "FAILURE") {
          echo 'Pipeline failed'
        }
      }
    }
  }
}

