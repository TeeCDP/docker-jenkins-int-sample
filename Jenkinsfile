pipeline {
  agent any
  stages {
    stage('Stage 2') {
      steps {
        sh 'echo deal1'
      }
    }

    stage('Archive') {
      parallel {
        stage('Archive') {
          steps {
            archiveArtifacts(artifacts: '*.*', fingerprint: true)
          }
        }

        stage('error') {
          steps {
            sh 'echo deal2'
          }
        }

      }
    }

    stage('error') {
      steps {
        sh 'echo deal3'
      }
    }

  }
}