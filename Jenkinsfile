pipeline {
    agent none
    stages {
	
	stage('Non-Parallel Stage') {
	    agent {
                        label "master"
                }
        steps {
                echo 'This stage will be executed first'
                }
        }

	stage('Build On Master') {
                    agent {
                        label "master"
                    }
                    steps {
						echo "Build on Master"
						bat 'Build.bat'
					}
        }
    
		
	
    }
}




