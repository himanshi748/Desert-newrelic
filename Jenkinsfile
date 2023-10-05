pipeline{
    agent any
    environment{
        entityGuid = 'MzYyNzM0NXxCUk9XU0VSfEFQUExJQ0FUSU9OfDExMjAyMzc1OTU'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test-One') {
            steps {
                echo 'Testing-One-1..'
            }
        }
        stage('Test-Two') {
            steps {
                echo 'Testing-Two-2..'
            }
        }
        stage('Test-Three') {
            steps {
                echo 'Testing-Three-3..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }

        stage('Post to New Relic') {
            steps{
                script {
                step([$class: 'NewRelicDeploymentNotifier', notifications: [[
                    apiKey: 'NRAK-OTDFMH5G2LAZE5VWOZ0WRBJ5TMA',
                    applicationId: '1120237595', 
                    changelog: 'test log', 
                    commit: 'added multiple test number', 
                    deeplink: '', 
                    deploymentId: '', 
                    deploymentType: 'BLUE_GREEN', 
                    description: 'Testing Tracker', 
                    entityGuid: '${entityGuid}', 
                    groupId: '78641', 
                    revision: 'Revision-one', 
                    timestamp: '', 
                    user: 'Himanshi Satpute', 
                    version: '1']]])
                }
            }
        }
    }
}