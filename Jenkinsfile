pipeline {
  agent any
  stages {
    stage ("Git Clone") {
      steps {
        git 'https://github.com/hamdaniw80/mysql-transkrip.git'
      }
    }
    stage ("Remove Image") {
      steps {
        sh "kubectl apply -f deployment.yaml"
      }
    }
    stage ("Clean workspaces") {
      steps {
        sh "rm -rf *"
      }
    }
  }
}