pipeline {
         agent any
         stages {
                 stage('1. Building Code...') {
                   steps {
                     echo "Building Code..."
                   }
                 }
                 stage('2. Unit Testing...') {
                   steps {
                     echo "Unit Testing..."
                   }
                 }
                 stage('3. Integration Testing...') {
                   steps {
                       echo "Integration Testing..."
                   }
                 }
                 stage('4. Integration and Acceptance Testing...') {
                    parallel { 
                             stage('Integration Testing') {
                                steps {
                                  echo "Running the integration test..."
                                }
                             }
                             stage('System test') {
                               steps {
                                 echo "Acceptance Testing..."
                              }
                            }
                   }
               }
                 stage('5. Deployment Testing...') {
                   steps {
                       echo "Deployment..."
                   }
                 }
       }
} 