pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'robot --outputdir $WORKSPACE -x  my_junit_format_log.xml /test.robot'
        xunit([JUnit(deleteOutputFiles: true, failIfNotNew: true, pattern: 'my_junit_format_log.xml', skipNoTestFiles: false, stopProcessingIfError: true)])
      }
    }
  }
}
