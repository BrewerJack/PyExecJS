pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'robot --outputdir / -x  my_junit_format_log.xml /test.robot'
        step([$class: 'XUnitBuilder', thresholds: [
        [$class: 'SkippedThreshold', failureThreshold: '0'],
        [$class: 'FailedThreshold', failureThreshold: '0']],
          tools: [[$class: 'JUnitType', pattern: 'reports/**']]])
        }
      }
    }
  }
}
