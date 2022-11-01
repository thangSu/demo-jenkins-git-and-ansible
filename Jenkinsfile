node{
  stage("SCM Checkout"){
    git 'https://github.com/thangSu/helloworld.git'
  }
  stage('compile and package'){
   def mvnHome = tool name: 'maven3', type: 'maven'
   sh '${mvnHome}/bin/mvn package'
  }
}
