pipeline {
	agent any
	environment {EXECUTE = true }
	stages {
		stage ('First') {
			steps {
				sh 'echo "First "'
			}
		}
		stage ('Twoe') {
			when { expression {EXECUTE}}
			steps {
                                sh 'echo "step Two"'
				sh 'echo "Updating Second Stage"'
                        }
                }
		stage ('Third') {
			when { expression {EXECUTE == false}}
			steps {
                                sh 'echo "Third"'
                        }
                }
	}
}
