env.MYTOOL_VERSION = '1.33'
pipeline {
	agent {label 'slave1'}  
    stages {
      stage ('Get Code From GIT') {
      	steps{ checkout scm 
            }
    }
       	stage ('build') {
      		steps{ mvn build
    }
 }
       	stage ('test') {
      		steps{ mvn test
    }
 }
}
}
