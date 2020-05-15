pipeline {
  agent any
  stages {
    stage('Lint HTML.') {
      steps {
        sh 'tidy -q -e *.html'
      }
    }

    stage('Upload to AWS.') {
      steps {
        withAWS(region: 'us-west-2', credentials: 'Nour') {
          s3Upload(file: 'index.html', bucket: 'nouran.portfolio', path: 'root.html')
        }

        sh 'echo "Hello World"'
        sh '''
                        echo "Multiline shell steps works too"
                        ls -lah
                    '''
      }
    }

  }
}
