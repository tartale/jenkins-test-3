pipeline {
   agent any
   options {
       timestamps()
       disableConcurrentBuilds()
       timeout(time: 2, unit: 'HOURS')
   }
   
   parameters {
     string(
       name: 'STATEMENT', 
       defaultValue: 'Everything is awesome!',
       description: 'Something to say'
     )
   }

   stages {

     stage('Integration tests') {
         when {
           expression { return params.RUN_INT_TESTS_STAGE }
         }
         steps {
            echo "Running integration tests.  ${params.STATEMENT}"
         }
     }
     stage('Openshift tests') {
         when {
           expression { return params.RUN_OPENSHIFT_TESTS_STAGE }
         }
         steps {
           echo "Running openshift tests  ${params.STATEMENT}"
         }
     }
   }
}
