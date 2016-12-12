stage('Dev') {
    node {
        echo 'hello from Pipeline'
        sh 'ls -al'
    }
}
stage('QA') {
    node {
        parallel(
            longerTests: {
                sh 'sleep 30'
            }, quickerTests: {
                sh 'sleep 10'
            }, evenquickerTests: {
                sh 'sleep 5'
            }
        )
    }
}
