node {
   def commit_id
   stage('Preparation') {
     checkout scm
     sh "git rev-parse --short HEAD > .git/commit-id"
     commit_id = readFile('.git/commit-id').trim()
   }
   stage('dockerbuild') {
     //def app = docker.build("yanivomc/docker-nodejs-demo:${commit_id}", '.'a
     echo "build"
     
   }
   stage('sonarqube tests') {
      //def app = docker.build("yanivomc/sonar:${commit_id}", '-f sonarbuild' , '.')                             
      echo "sonar"
     
   }                                     
   //stage('docker build/push') {            
   //  docker.withRegistry('https://index.docker.io/v1/', 'dockerhub') {
    //   def app = docker.build("yanivomc/docker-nodejs-demo:${commit_id}", '.').push()
    // }                                     
   //}     
}      

