pipeline { 
    agent any 
    stages {
        stage('Build') { 
                sh 'make publish'
                sh '''
                 echo "Multi-line shell steps"
                 ls -lah
                 '''
            }
        }
    }
}
