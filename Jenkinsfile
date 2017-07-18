pipeline {
  agent any
  stages {
    stage('Install') {
      steps {
        sh 'echo Install stage'
        dir('tests') {
            git url: 'github-tests:futurestay/Codeception_Test_Repo.git'
        }
        dir('tests/_data') {
            sh '$(gunzip -c ./futurest_main.sql.gz | mysql -uroot futurest_main)'
            sh '$(gunzip -c ./futurest_FS12497.sql.gz | mysql -uroot futurest_FS12497)'
        }
      }
    }
    stage('Build') {
      steps {
        sh 'echo Build stage'
        sh 'touch build_stage_file'
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
