node {
    stage('Build') {
        sh 'echo "Hello World"'
        sh '''
            echo "Multiline shell steps works too"
            ls -lah
        '''
    }

    stage('Deploy') {
        steps {
           timeout(time: 3, unit: 'MINUTES') {
              retry(5) {
                  echo "deploy thing"
               }
           }
      }
    }
}

