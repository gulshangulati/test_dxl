#!/usr/bin/env groovy
pipeline {

    agent any
    stages {
        stage ('one')
        {
        agent {
        label "kubectl"
             }
          steps 
          {
        container('kubectl') 
        {
          sh 'which kubectl'

                  }
         }
        }
        stage ('two stepp')
        {
            agent {
        label "kubectl"
      }
      steps {
        container('kubectl') {
          sh 'which kubectl'
        script {

            def no_pods
            sh """
            kubectl get pods -n dev
            kubectl get pods -n chatbot-preprod-uk 
            """
             }
        }
      }
             
    }
}
}

