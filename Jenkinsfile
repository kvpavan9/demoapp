node  {
stage('Fetch Code Staging') {
  sh('git clone https://github.com/kvpavan9/demoapp.git')
  sh('pwd')
}
//Stage 1 : Build the docker image.

stage('Build image') {
  sh('docker build -t ureg-docvault .')
  sh('sudo docker tag ureg-docvault:latest 201013321275.dkr.ecr.ap-southeast-1.amazonaws.com/ureg-docvault:latest')

}

//Stage 2 : Push the image to GCR
stage('Push image to registry') {
  sh('sudo docker push 201013321275.dkr.ecr.ap-southeast-1.amazonaws.com/ureg-docvault:latest')
}

}
   
