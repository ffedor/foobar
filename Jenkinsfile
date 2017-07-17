pipeline {
  agent any
  stages {
    stage('Install') {
      steps {
        sh 'echo Install stage'
        dir('tests') {
            git url: 'github-tests:futurestay/Codeception_Test_Repo.git'
        }
      }
    }
    stage('Build') {
      steps {
        sh 'echo Build stage'
      }
    }
    stage('Test') {
      steps {
        sh 'echo Test stage'
      }
    }
    stage('Fini') {
      steps {
        sh 'echo Fini stage'
      }
    }
  }
}
