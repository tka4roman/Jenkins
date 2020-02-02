pipeline {
    agent any
    stages {
        stage('GIT Repo') {
            steps {
                sh 'pwd'
		checkout([$class: 'GitSCM', branches: [[name: 'refs/remotes/origin/*_test']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/tka4roman/Jenkins']]])
            }
        }
	stage("Build HW") {
	    steps {
		sh 'pwd'
		sh './hello.py'
	    }
	}
	stage('Report hash') {
	    steps {
		sh 'pwd'
		sh 'echo "Your commit is: $(git log -1 --pretty=tformat:%h)"'
    	    }
	}
    }
}

