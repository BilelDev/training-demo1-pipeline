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
           
    
        stage('Run Tests') {
            parallel {
                stage('Test On Windows') {
                    agent {
                        label "Windows_Node"
                    }
                    steps {
                        echo "Test on Agent"
						bat 'Unit.bat'
                    }
                    
                }
                stage('Test On Master') {
                    agent {
                        label "master"
                    }
                    steps {
						echo "Test on Master"
						bat 'Unit.bat'
					}
                }
            }
        }
		
	
    }
}
