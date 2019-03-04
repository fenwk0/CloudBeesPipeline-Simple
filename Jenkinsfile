pipeline {
  agent any
  stages {
    stage('initialise') {
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
    stage('deploy') {
      parallel {
        stage('vaidate') {
          steps {
            echo 'bye'
          }
        }
        stage('error') {
          steps {
            sleep 2
            echo 'parallel step'
          }
        }
      }
    }
    stage('status') {
      steps {
        echo 'performing health checks'
        sleep 2
        echo 'health checks complete'
      }
    }
    stage('load') {
      steps {
        echo 'load system'
        sleep 2
        echo 'load test finished'
      }
    }
  }
}