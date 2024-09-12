pipeline {
    agent {
    // this image provides everything needed to run Cypress
        docker {
            image 'cypress/browsers'
        }
     }
    
     // Définir un déclencheur pour exécuter le pipeline toutes les 3 minutes
    triggers {
        cron('H/3 * * * *') // Toutes les 3 minutes
    }
    
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
