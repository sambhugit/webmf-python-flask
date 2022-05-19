pipeline {
  agent { docker { image 'python:3.8.10' } }
  stages {
    stage('build') {
      steps {
        sh 'echo buildddd'
      }
    }
    stage('test') {
      steps {
        sh 'python test.py'
      }
      post {
        always {
          junit 'test-reports/*.xml'
        }
      }    
    }
  }
}
