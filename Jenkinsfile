node{
   
   stage("App Build started"){
      echo 'App build started..'
      git credentialsId: 'Github-ID', url: 'https://github.com/InfinityVegas/python-docker-app-openshifts.git'
      }
   
   stage('Docker Build') {
     def app = docker.build "manee2k6/python-app"
    }
   
   stage("Tag & Push image"){
      withDockerRegistry([credentialsId: 'Github-ID', url: 'https://index.docker.io/v1/']) {
          sh 'docker tag manee2k6/python-app manee2k6/python-app:poornima_001'
          sh 'docker push manee2k6/python-app:poornima_001'
          sh 'docker push manee2k6/python-app:latest'
      }
    }
   
   stage("App deployment started"){
      echo 'App deployment started to Openshift environment..'
     //sh 'oc login https://api.starter-us-west-1.openshift.com --token=l334xAzzGBl7kvYuUFcvfRCCXMsQxeQJox3pEzbSQrQ'
     //sh 'oc new project padmavathy'
     //sh 'oc new-app manee2k6/python-app:pattabhi-1.0 --name python-app'
     //sh 'oc expose svc python-app --name=python-app'
     //sh 'oc status'
    }
   
    stage('App deployed to Openshift environment') {
     echo 'App deployed to Openshift environment..'
    }

   
























}
