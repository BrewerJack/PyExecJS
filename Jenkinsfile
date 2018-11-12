pipeline {
  agent any
  stages {
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh 'robot --outputdir / -x  my_junit_format_log.xml /test.robot'
            step([$class: 'XUnitBuilder',
                        thresholds: [[$class: 'FailedThreshold', unstableThreshold: '1']],
                        tools: [[$class: 'XUnitDotNetTestType', pattern: '/my_junit_format_log.xml']]])
          }
        }
        stage('') {
          steps {
            sh '''echo $WORKSPACE
'''
          }
        }
      }
    }
  }
}