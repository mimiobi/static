pipeline {
  agent any 
  stages {
    stage('Upload to AWS') {
      steps {
          withAWS(credentials:'aws-static') { 
                    s3Upload(file:'index.html', bucket:'staticjenkins', path:'')
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
