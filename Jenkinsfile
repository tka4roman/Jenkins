pipeline {
    agent any
    stages {
        stage('GIT Repo') {
            steps {
                sh 'cd /home/rtk/Documents/JenkinsProj/Jenkins'
                sh 'git pull'
                sh 'pwd'
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

