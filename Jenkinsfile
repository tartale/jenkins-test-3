pipeline {
   agent any
   options {
       timestamps()
       disableConcurrentBuilds()
       timeout(time: 2, unit: 'HOURS')
   }

   stages {

     stage('Integration tests') {
         when {
           expression { return params.RUN_INT_TESTS_STAGE }
         }
         steps {
           echo "Running integration tests"
         }
     }
     stage('Openshift tests') {
         when {
           expression { return params.RUN_OPENSHIFT_TESTS_STAGE }
         }
         steps {
           echo "Running openshift tests"
         }
     }
   }
}
