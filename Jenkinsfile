pipeline {
   agent any
   options {
       timestamps()
       disableConcurrentBuilds()
       timeout(time: 2, unit: 'HOURS')
   }

   stages {

     stage('Say Goodbye') {
         steps {
           echo "Goodbye ${env.YOURNAME}.  Everything sucks!"
         }
     }
   }
}

