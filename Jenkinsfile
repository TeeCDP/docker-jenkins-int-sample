pipeline {
  agent any
  stages {
    stage('Stage 2') {
      steps {
        sh 'echo deal1'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts(artifacts: '*.*', fingerprint: true)
      }
    }

    stage('error') {
      steps {
        copyArtifacts(projectName: 'jenkins-docker-int', fingerprintArtifacts: true)
      }
    }

  }
}