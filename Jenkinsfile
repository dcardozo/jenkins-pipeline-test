pipeline {
  agent any
  stages {
    stage('Display Pipeline Info') {
      steps {
        sh 'echo "Workspace is ${WORKSPACE}"'
      }
    }
    stage('PWD') {
      steps {
        pwd()
      }
    }
    stage('Sleep 10, then ls -1') {
      steps {
        sleep 10
        sh 'ls -1'
      }
    }
    stage('Display PROP1 value') {
      steps {
        sh 'echo "PROP1 value is ${PROP1}"'
      }
    }
  }
  environment {
    PROP1 = 'val1'
  }
}