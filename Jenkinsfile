node{

stage('Fetch Code Staging') {
  sh "git clone https://github.com/RahulSK1807/demoapp.git"
  sh "pwd"
}
//Stage 1 : Build the docker image.

stage('Build image') {
  sh "sudo docker build -t asia.gcr.io/fabhotels-development/demoapp ."
}

//Stage 2 : Push the image to GCR
stage('Push image to registry') {
  sh "gcloud auth configure-docker"
  sh "sudo docker push asia.gcr.io/fabhotels-development/demoapp"
  }
 }    
}
