pipeline {
   environment {
	   MavenHome = tool 'M3'
	   URLJENKINS="${env.HUDSON_URL}"
	   BRANCH="${env.GIT_BRANCH}"
   }
    agent any
    options {
        skipStagesAfterUnstable()
	    
    }
    stages {
        stage ('Example') {
		steps {
			script{
				log.info ('JUG : Starting The Example Stage')
				unit_test()
				build()
				static_code_analysis()
				//GetProjectID() works only with maven
			}
		}
	}
    }
}
	

         

    
        
