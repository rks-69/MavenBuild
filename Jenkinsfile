pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        bat '''
        @echo off
        echo Hello. World!
        '''
      }
    }
    stage('hello') {
      steps {
        bat '''
        @echo off
        echo Executing from Powershell!
        '''
      }
    }
  }
}
