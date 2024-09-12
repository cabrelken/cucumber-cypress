pipeline {
    agent {
    // this image provides everything needed to run Cypress
        docker {
            image 'cypress/browsers'
        }
     }
    
    // triggers {
    //     cron('H/3 * * * *') // Toutes les 3 minutes
    // }
    
    stages {
        stage('Install dependencies') {
            steps {
                sh 'npm ci'
            }
        }
        
        
        stage('Run Cypress Tests') {
            steps {
                
                sh "npm run cy:run"
             }
        }
    }  
 
}
