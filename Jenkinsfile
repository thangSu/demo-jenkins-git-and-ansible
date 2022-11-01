node{
  stage("SCM Checkout"){
    git 'https://github.com/thangSu/helloworld.git'
  }
  stage('compile and package'){
   def mvnHome = tool name: 'maven3', type: 'maven'
   sh "${mvnHome}/bin/mvn package"
  }
  stage('email notification'){
    mail bcc: '', body: '''Hi welcome to jenkins email alerts
    thanks
    Thang''', cc: '', from: '', replyTo: '', subject: 'jenkins jobs', to: 'phamthang3003@gmail.com'
  }
}
