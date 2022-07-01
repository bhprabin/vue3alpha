pipeline {
    environment {
        MSG = "Building!"
    }

    agent none
    stages {
	    stage("Build") {
			steps {
                sh "echo ${MSG}"
            }
	    }
    }
}