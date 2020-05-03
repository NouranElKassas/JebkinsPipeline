pipeline { 
    agent any 
    stages {
        stage('Build') { 
                sh 'echo "Hello World"'
                sh '''
                 echo "Multi-line shell steps"
                 ls -lah
                 '''
            }
        }
    }
}
