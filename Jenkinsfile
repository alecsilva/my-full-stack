pipeline {
  agent {label "linux"}
  stages {
    stage('Hola') {
      steps {
	echo "hola desde Jenkinsfile"
      }
    }
    stage('for the fix branch'){
      when {
	branch "fix-*"
      }
      steps {
	sh '''
	  cat README.md
	'''
      }
    }
    stage('for the PR') {
      when {
	branch 'PR-*'
      }
      steps {
	echo 'this only runs for the PRs'
      }
    }
  }
}
