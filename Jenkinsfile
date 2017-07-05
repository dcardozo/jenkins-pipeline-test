pipeline {
  agent any
  stages {
    stage('Display Pipeline Info') {
      steps {
        echo 'Workspace is ${env.WORKSPACE}'
      }
    }
    stage('PWD') {
      steps {
        pwd()
      }
    }
    stage('Sleep, then ls -1') {
      steps {
        parallel(
          "Sleep 10, then ls -1": {
            sleep 10
            sh 'ls -1'
            
          },
          "Sleep 15, then pwd again": {
            sleep 15
            sh 'pwd'
            
          }
        )
      }
    }
  }
}