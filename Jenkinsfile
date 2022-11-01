 tools{
   maven 'maven3'
 }
node{
  stage("SCM Checkout"){
    git 'https://github.com/thangSu/helloworld.git'
  }
  stage('compile and package'){
    sh 'mvn packge'
  }
}
