pipeline {
   agent any
   options {
       timestamps()
       disableConcurrentBuilds()
       timeout(time: 2, unit: 'HOURS')
   }

   stages {

     stage('Say What?') {
         steps {
           echo "What's going on ${params.YOURNAME}?"
         }
     }
   }
}

