pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sh 'robot --outputdir / -x  my_junit_format_log.xml /test.robot'
      }
    }
    stage('test2') {
      steps {
        sh 'cd /; echo $PWD'
      }
    }
  }
}