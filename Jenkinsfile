node{
 stage('SCM Checkout')
    {
        git credentialsId: 'f83ee8b5-b4b2-420e-892b-d341e313c937', url: 'https://github.com/BilelDev/training-demo1-pipeline.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'docker-compose build'
      
    }
  
}
