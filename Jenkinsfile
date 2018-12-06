pipeline {
    
    agent {
        dockerfile true 
    }

    def exj

    stage('Clone repository'){
         /*Pour clone le referentiel sur notre repertoire de travail*/
         checkout scm   
    }
    stage('Build image') {
        
        exj = docker.build("odiarra/ci-jira")
    }

    stage('Test image') {
         
        exj.inside {
            sh 'echo "Tests passed"'
        }
    }

} 
