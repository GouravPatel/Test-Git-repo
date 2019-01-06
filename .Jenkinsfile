#!groovy​

pipeline {
    agent any

    environment {
        DEPLOY_HOST = '69.20.99.172'
        DEPLOY_DOC_ROOT = '/var/www/jenkins-demo/'
        DEPLOY_USER = 'gourav-patel'
    }
    
    stages {
        stage('Deploy') {
            steps {
                
                sh "ssh -o StrictHostKeyChecking=no $DEPLOY_USER@$DEPLOY_HOST \"cd $DEPLOY_DOC_ROOT && git fetch origin -key '/home/gourav-patel/' && git reset --hard origin/master\""
            }
        }
    }
}
