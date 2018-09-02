node('slave') {
   stage ('Checkout'){
      checkout scm
   }
   stage ('Build Maven'){
      def mvnHome = tool 'maven3'
      sh "${mvnHome}/bin/mvn clean install"
   }
   stage ('Test Maven'){
      def mvnHome = tool 'maven3'
      sh -x "${mvnHome}/bin/mvn clean test"
   }
	
}
