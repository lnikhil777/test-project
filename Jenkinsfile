pipeline {
  agent any;
  stages {
    stage ('BUILD') {
      steps {
        echo "this is a build stage"
      }
    }

    stage ( 'test parallel') {
    parallel {
      stage ('test on chrome 1') {
      steps  {
        echo "testing on server 1)"

      }
      }
      stage ('test on server 2') {
        steps {
          echo "testing on server 2"
        }
      }
    }
    }
  }
}
    
