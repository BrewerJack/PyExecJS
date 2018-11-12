pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sh 'robot --outputdir / -x  my_junit_format_log.xml /test.robot; junit /my_junit_format_log.xml'
      }
    }
  }
}