pipeline{
    agent any
      tools{
        maven 'mvn-sat'
       jdk 'java-sat'
     }
     stages{
         
         stage ('checkout') {
             steps {
                 echo "hi"
                 git 'https://github.com/devopsstephen/monay.git'
             }
         }
    
     
    stage ('Build project') {
       steps {
         
       sh 'mvn clean package'
 
      
   }
}

 stage ('deploy') {
       steps {
         
       sh '/opt/deploy.sh'
 
      
   }
}
stage ('mail') {
    steps {
       mail bcc: '', body: 'jenkins job success ', cc: '', from: '', replyTo: '', subject: 'jenkinsjob', to: 'theetisatish@gmail.com'
    }

    }
}
    
}

