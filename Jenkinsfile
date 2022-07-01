pipeline {
    environment {
        MSG = "Building!"
    }

    agent any
    stages {
	    stage("Build") {
			steps {
                sh "echo ${MSG}"
            }
	    }
    }
}