pipeline {
  // agent server1/any/dockeragent/kubernetes
  agent any 
  parameters {
  choice choices: ['dev', 'sit', 'uat', 'pt', 'preprod', 'prod'], 
  description: 'Select the environment', name: 'ENV'
  }
  environment {
    JAVA_HOME = "/opt/java/myjava/bin"
  }
  

  stages {
    stage("working with variables") {
      steps {
          script {
            var1=100
            println "var1 value is ${var1}"
            println "WORKSPACE is ${WORKSPACE}"
            println "BUILD_NUMBER is ${BUILD_NUMBER}"
            println "my environment selected  is ${params.ENV}"
            println "my JAVA_HOME value is ${env.JAVA_HOME}"
          }
        }
      }
    }
}  
