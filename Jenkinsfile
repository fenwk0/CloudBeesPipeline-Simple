pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build-image') {
          steps {
            sleep 5
            echo 'Building new image'
          }
        }
        stage('build-config') {
          steps {
            echo 'Creating test config'
          }
        }
        stage('populate-data-source') {
          steps {
            echo 'Drop tables'
          }
        }
      }
    }
    stage('validate') {
      parallel {
        stage('vaidate') {
          steps {
            echo 'bye'
          }
        }
        stage('') {
          steps {
            sleep 2
            echo 'parallel step'
          }
        }
      }
    }
  }
}