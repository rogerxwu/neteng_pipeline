pipeline {
    agent { dockerfile true }
    environment {
        EXAMPLE_CREDS = credentials('cred_vsrx_192_168_223_2')
    }
    stages {
        stage('Test') {
            steps {
                sh 'python3 -V'
                //$EXAMPLE_CREDS_USR
                //$EXAMPLE_CREDS_PSW
                //sh 'python3 deploy_to_network.py -username'
                sh 'python3 test.py -username $EXAMPLE_CREDS_USR -password $EXAMPLE_CREDS_PSW'
            }
        }
    }
}