pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'robot --outputdir / -x  my_junit_format_log.xml /test.robot'
        xunit(testTimeMargin: '100', thresholdMode: 100, testDataPublishers: '/my_junit_format_log.xml')
      }
    }
  }
}