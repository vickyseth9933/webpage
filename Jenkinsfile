node {
    def app

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */

        app = docker.build("vickyseth9933/webpage")
    }

    stage('Test image') {
        /* Ideally, we would run a test framework against our image.
         * Just an example */

        app.inside {
            sh 'echo "Tests passed"'
        }
    }
}
