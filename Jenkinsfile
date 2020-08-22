pipeline {

  agent { label 'kubepod' }

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/Aryan-gupta4460/playjenkins.git', branch:'test-deploy-stage'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
