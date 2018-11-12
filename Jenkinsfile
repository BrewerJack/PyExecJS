pipeline {
  agent any
  stages {
    stage('') {
      steps {
        sh 'robot --outputdir / -x  my_junit_format_log.xml /test.robot'
        junit(healthScaleFactor: 1, testResults: '/my_junit_format_log.xml')
      }
    }
  }
}