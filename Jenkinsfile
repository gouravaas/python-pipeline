pipeline {
	agent {
		label "Pipeline-slave"
	}
	stages{
		stage ( "pull scm" ){
			steps {
				git branch: 'python', url: 'https://github.com/gouravaas/python-pipeline.git'	
			}
		}
		stage {
			steps ("Build"){
				sh 'python -v'
				sh 'python cp.py'
			}
		}
		stage {
			steps ("test"){
				sh 'python test.py'
			}
		}
	}
}
