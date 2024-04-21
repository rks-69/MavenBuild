pipeline {
  agent any
  stages {
    stage('Code Checkout'){
		checkout changelog: false, poll: false, scm: scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'GitHubCreds', url: 'https://github.com/rks-69/MavenBuild']])
	}
    stage('Maven Build') {
      steps {
        bat '''
        @echo off
        call mvn clean install
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
