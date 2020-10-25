node ('master'){  
    def app
    stage('Cloning Git') {
        /* Let's make sure we have the repository cloned to our workspace */
       checkout scm
    }  
   /* stage('SAST'){
        build 'SECURITY-SAST-SNYK'
    } */

    stage('Build-and-Tag') {
    /* This builds the actual image; synonymous to
         * docker build on the command line */
        sh 'echo Buillding test'
        //app = docker.build("amrit96/snake")
    }
    stage('Post-to-dockerhub') {
        sh 'echo test_post_to_dockerhub'
     /*docker.withRegistry('https://registry.hub.docker.com', 'training_creds') {
            app.push("latest")
        			}*/
         }
   /* stage('SECURITY-IMAGE-SCANNER'){
        build 'SECURITY-IMAGE-SCANNER-AQUAMICROSCANNER'
    } */
  
    stage('Pull-image-server') {
        sh 'echo pull'
        /* sh "docker-compose down"
         sh "docker-compose up -d" */	
      }
    
    /*stage('DAST')
        {
        build 'SECURITY-DAST-OWASP_ZAP'
        }*/
 
}
