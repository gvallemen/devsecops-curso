pipeline {
  agent any

  stages {

    stage('git version') {
      steps {
        sh "git version"
      }
    }

    stage('maven version') {
      steps {
        sh "mvn -v"
      }
    }

    stage('docker version') {
      steps {
        sh "docker -v"
      }
    }
    //****Checar llaves de archivo kubeconfig
    stage('kubernetes version') {
      steps {
        withKubeConfig([credentialsId: 'kubeconfig']) {
          sh "kubectl version --short"
        }
      }
    }
  }
}
