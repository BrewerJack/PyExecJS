pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'robot --outputdir / -x  my_junit_format_log.xml /test.robot'
        xunit(testTimeMargin: '0', testDataPublishers: '/my_junit_format_log.xml')
      }
    }
  }
}