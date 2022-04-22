pipeline {
    agent any

	environment {
		svn_path='file:///C:/Users/hirose.yuri/Desktop/WORK/00_プロジェクト資料/022204_アイシン/TEST_SVN/repo'
	}

    stages {
        stage('Hello') {
            steps {
                echo 'Hello'
            }
        }
        stage('Mail') {
            steps {
                mail bcc: '', body: 'This is a test', cc: '', from: 'hirose.yuri@pphrp-technology.jp', replyTo: '', subject: 'Jenkins-TEST mail', to: 'hirose.yuri@pphrp-technology.jp'
            }
        }
    }
}
