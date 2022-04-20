pipeline {
    agent any

	environment {
		svn_path='file:///C:/Users/hirose.yuri/Desktop/WORK/00_プロジェクト資料/022204_アイシン/TEST_SVN/repo'
	}

    stages {
        stage('Subversion') {
            steps {
                checkout([$class: 'SubversionSCM', additionalCredentials: [], excludedCommitMessages: '', excludedRegions: '', excludedRevprop: '', excludedUsers: '', filterChangelog: false, ignoreDirPropChanges: false, includedRegions: '', locations: [[cancelProcessOnExternalsFail: true, credentialsId: '', depthOption: 'infinity', ignoreExternalsOption: true, local: '.', remote: svn_path]], quietOperation: true, workspaceUpdater: [$class: 'UpdateUpdater']])
            }
        }
        stage('Mail') {
            steps {
                mail bcc: '', body: 'テストメールです', cc: '', from: 'hirose.yuri@pphrp-technology.jp', replyTo: '', subject: 'enkins-TEST mail', to: 'hirose.yuri@pphrp-technology.jp'
            }
        }
    }
}
