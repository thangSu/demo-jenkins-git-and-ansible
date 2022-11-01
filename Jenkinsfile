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
  stage('slack nofitication'){
    slackSend baseUrl: 'https://hooks.slack.com/services/', 
    channel: '#jenkins-pipline-demo', color: 'good', 
    message: 'welcome to jenkins, Slack!', 
    tokenCredentialId: 'slack-demo', 
    username: 'jenkins-job'
  }
}
