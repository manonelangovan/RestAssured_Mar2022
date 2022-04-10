pipeline {
  agent any
  stages {
    stage('dev build') {
      steps {
        echo 'dev done'
      }
    }

    stage('qa test') {
      parallel {
        stage('qa test') {
          steps {
            echo 'qa auto'
          }
        }

        stage('sele test') {
          steps {
            echo 'app test'
          }
        }

      }
    }

    stage('UAT') {
      steps {
        echo 'UAT test'
      }
    }

    stage('prod') {
      steps {
        input 'deploy to prod'
      }
    }

  }
}