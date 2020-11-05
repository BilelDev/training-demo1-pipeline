node{

    stage('SCM Checkout')
    {
        git credentialsId: 'fb38ae03-7d26-4e95-a2a2-c2e695405b22', url: 'https://github.com/BilelDev/training-demo1-pipeline.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u upasanatestdocker -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "upasanatestdocker" -p "Zephyr@17" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'sudo docker push upasanatestdocker/job1_web2.0'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
