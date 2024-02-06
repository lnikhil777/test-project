pipeline {
  agent any;
  stages {
    stage ('BUILD') {
      steps {
        echo "this is a build stage"
        sh 'sleep 5'
      }
    }

    stage ( 'test parallel') {
    parallel {
      stage ('test on chrome 1') {
      steps  {
        echo "testing on server 1)"
        sh 'sleep 5'

      }
      }
      stage ('test on server 2') {
        steps {
          echo "testing on server 2"
          sh 'sleep 5'
        }
      }
    }
    }
    stage ( 'deploy parallel') {
    parallel {
      stage ('deploy on server 1') {
      steps  {
        echo "deployed on server 1)"
        sh 'sleep 5'

      }
      }
      stage ('deploy on server 2') {
        steps {
          echo "deployed on server 2"
          sh 'sleep 5'
        }
      }
stage ('deploy on server 3') {
        steps {
          echo "deployed on server 3"
          sh 'sleep 5'
        }
      }
    }    
    } 
  }
}
    
