pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pwd
date
compile
test
build'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test'
          }
        }

        stage('test par') {
          steps {
            echo 'test par'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        sleep 10
      }
    }

  }
}