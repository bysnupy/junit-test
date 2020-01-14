pipeline {
     agent { node { label 'maven'} }
     stages {
         stage('checkout') {
           steps {
             git url: "https://github.com/bysnupy/junit-test.git"
           }
         }
         
         stage('maven availability') {
             steps {
                 sh "which mvn"
                 sh "mvn clean install"
                 sh "mvn test"
             }
         }
         stage('oc availability') {
             steps {
                 sh "which oc"
                 sh "oc whoami"
             }
         }
     }
 }
