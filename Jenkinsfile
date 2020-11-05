node{

    
    stage('Run Docker Compose File')
    {
        bat 'docker-compose build'
        bat 'docker-compose up -d'
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
             
             sh 'docker login -u "bileldaikhi007" -p "22605020" docker.io'
             //sh 'docker push upasanatestdocker/mysql'
             //sh 'docker push upasanatestdocker/job1_web1.0'
             sh 'docker push bileldaikhi007/training-demo1-pipeline'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
