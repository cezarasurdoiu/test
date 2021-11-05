pipeline {
    agent any
    triggers {
        pollSCM 'H/10 * * * *'
    }
    stages {
        stage('checkout') {
            steps {
                checkout([
                    $class: 'SubversionSCM', 
                    additionalCredentials: [], 
                    excludedCommitMessages: '', 
                    excludedRegions: '', 
                    excludedRevprop: '', 
                    excludedUsers: '', 
                    filterChangelog: false, 
                    ignoreDirPropChanges: false, 
                    includedRegions: '', 
                    locations: [[
                        credentialsId: '9beafea5-e7dc-473a-bc46-f2d3c381fb06', 
                        depthOption: 'infinity',
                        ignoreExternalsOption: true, 
                        local: '.', 
                        remote: 'http://172.31.0.3/svn/repo2']], 
                    workspaceUpdater: [$class: 'CheckoutUpdater']
                ])
            }
        }
    }
}
