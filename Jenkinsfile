pipeline {
  agent any
  stages {
     stage('sonar quality check') {
	   agent {
       docker {
         image 'maven'
                }
            }
	   steps{
       script{
	    withSonarQubeEnv(credentialsId: 'f2144c8a-adaf-436e-aba4-8e4cd35fbeca') {
		 sh 'mvn clean package'
		       }
          }
  }
}
}
}
