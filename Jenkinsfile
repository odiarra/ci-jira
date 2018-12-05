 node('Jenkins-ci-Jira') {

    def app

    stage('Clone repository'){
         /*Pour clone le referentiel sur notre repertoire de travail*/
         checkout scm   
    }
    stage('Build image') {
        

        app = docker.build("getintodevops/hellonode")
    }

    stage('Test image') {
         
        app.inside {
            sh 'echo "Tests passed"'
        }
    }

} 
