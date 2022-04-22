pipeline {
 agent any
  stages {
    stage("git") {
      steps {
        echo "Check out GitHub"
        git branch: 'main', url: 'https://github.com/dprzegal/website2.git'
      }
    }
    stage("deploy") {
      steps {
        echo "Deploy to Nginx webserver"
        sh 'rsync -avh /var/lib/jenkins/workspace/pipelineviaJenkinsfile2/* /var/www/website/'
      }
    }
  }
}
