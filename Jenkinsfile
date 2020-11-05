node{

    stage('SCM Checkout')
    {
        git credentialsId: 'f83ee8b5-b4b2-420e-892b-d341e313c937', url: 'https://github.com/BilelDev/training-demo1-pipeline.git'
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
            sh "docker login -u bileldaikhi007 -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "bileldaikhi007" -p "22605020" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'sudo docker push bileldaikhi007/training-demo1-pipeline'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
