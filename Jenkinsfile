node('slave') {
   // Mark the code checkout 'stage'....
   stage ('Checkout'){

      // Get some code from a GitHub repository
      checkout scm
   }
   // Mark the code build 'stage'....
   stage ('Build Maven'){
      // Get the maven tool.
      // ** NOTE: This 'maven3' maven tool must be configured
      // **       in the global configuration.
      def mvnHome = tool 'maven3'
      // Run the maven build
      sh "${mvnHome}/bin/mvn clean install"
   }
   // Mark the code build 'stage'....
   stage ('Test Maven'){
      // Get the maven tool.
      // ** NOTE: This 'maven3' maven tool must be configured
      // **       in the global configuration.
      def mvnHome = tool 'maven3'
      // Run the maven test
      sh "${mvnHome}/bin/mvn clean test"
   }
	
}
