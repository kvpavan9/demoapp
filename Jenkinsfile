node {
    def app

    stage('Clone repository') {
        /* repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* To builds the dockerimage */
        //update your ECR registry URI
        app = docker.build("https://asia.gcr.io/fabhotel-developement/demoapp")
    }

    stage('Test image') {
        /* Try killing some white walkers for testing ;-) */

        app.inside {
            sh 'echo "Hurray !! Tests passed, Valar Morghulis "'
        }
    }

}
