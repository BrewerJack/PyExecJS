pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'robot --outputdir $WORKSPACE -x  my_junit_format_log.xml /test.robot'
        xunit(testDataPublishers: 'XUnitDotNetTestType')
      }
    }
  }
}