pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
	}
	stage('Test') {
   	    steps {
        	sh 'test -s index.html'
        	sh 'grep "Hello from my own CI/CD pipeline!" index.html'
    	    }
	}
	stage('Deploy') {
	    steps {
		sh 'cp index.html /var/www/soumaditya-static/index.html'	 
	    }
	}
}
}
