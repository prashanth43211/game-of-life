pipeline {
   agent any
 

   tools {
      // Install the Maven version configured as "M3" and add it to the path.
      jdk 'Java8'
      maven "Maven3.3.9"
   }
   
   stages
   {
   stage('git clone') {
         steps {
            // Get some code from a GitHub repository
		 
          sh  '''
	  sudo sudo rm -rf /home/ubuntu/Copy/try
          sudo git init
	  sudo git clone https://github.com/prashanth43211/game-of-life.git
          '''
        }
        
        }
	stage ('Compile and Build') {
         steps {
           sh 'mvn clean install -U  -Dmaven.test.skip=true'
           
         }
	}
   }
}
