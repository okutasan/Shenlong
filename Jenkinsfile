pipeline {
  agent {
    docker {
      image 'openjdk:8-alpine'
      args '-v /tmp:/tmp'
      reuseNode true
    }
  }
  options {
        copyArtifactPermission('mtarget-backend/*');
    }
  stages {
    stage('Build') {
      steps {
        echo 'Copy Artifact'
        copyArtifacts(projectName: 'gorosei/jenkins');
      }
    }

  }
}
