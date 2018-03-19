pipeline{
  agent any
  tools {
    jdk 'JDK1.8.0'
  }
  environment{
    SPARK_ROOM = "e54d06a0-223d-11e8-925b-e97814520571"
    ARTIFACT_ID = "hello-cloud-web-app-angular"
    PROJECT_VERSION = "2018.3.1"
  }
  stages{
    stage ('Build'){
      steps {
        notifyBuildStart()
        sh 'npm install'
      }
    }
  }
  post {
	always {
		    notifyBuildEnd()
		}
	}
}