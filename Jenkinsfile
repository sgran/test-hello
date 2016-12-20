stage('Dev') {
    node('mesos') {
        echo 'hello from Pipeline'
        sh 'ls -al'
        sh 'hostname -f'
        sh 'pwd'
        sh 'false'
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
