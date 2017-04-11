pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(changelog: true, url: 'https://github.com/manlme/moxie', branch: '$params.VERSION', poll: true)
      }
    }
    stage('deploy') {
      steps {
        sh 'scp'
        echo 'successfully uploaded.'
        sh 'ssh'
        emailext(subject: 'deploy xxx successfully', body: 'deploy xxx successfully', to: 'mosquito.blood@hotmail.com', replyTo: 'mosqiuto.blood@hotmail.com')
      }
    }
  }
}