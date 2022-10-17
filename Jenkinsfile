pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'docker pull 090380/eureka-services-1:latest'
      }
    }

    stage('deploykubernetes') {
      steps {
        sh 'kubectl create deployment eureka-services --image=090380/eureka-services-1:latest --replicas=1'
      }
    }

  }
}