node{
   stage('SCM Checkout'){
     git 'https://github.com/deepakteja/my-app.git'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'maven 3', type: 'maven'  
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Email Notification'){
      mail bcc: '', body: '''Build is success

      Regards,
      T''', cc: '', from: '', replyTo: '', subject: 'Build success', to: 'dev.deepakteja@gmail.com'
   }
}


