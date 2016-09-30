node {
    
    stage 'Code'
    checkout scm

    def package_name = sh (
        script: 'git config --get remote.origin.url | grep -o "github.com.*"',
        returnStdout: true
    )

    stage 'Check Conflicts'
    //sh "./build/steps/deploy/check-conflicts.sh"
    
    stage 'Merge Pull Request'
    //sh "./build/steps/deploy/merge.sh"

    // https://api.github.com/repos/aerian-studios/githubflow-test/pulls/1

    // /repos/:owner/:repo/pulls/CHANGE_ID

    echo "package_name: ${package_name}"
    echo "JOB_NAME: ${JOB_NAME}"
    echo "JOB_BASE_NAME: ${JOB_BASE_NAME}"
    echo "BRANCH_NAME: ${BRANCH_NAME}"
    echo "CHANGE_TARGET: ${CHANGE_TARGET}"
    echo "CHANGE_ID: ${CHANGE_ID}"
    echo "CHANGE_URL: ${CHANGE_URL}"
    echo "CHANGE_TITLE: ${CHANGE_TITLE}"
    echo "CHANGE_AUTHOR: ${CHANGE_AUTHOR}"
    echo "CHANGE_AUTHOR_DISPLAY_NAME: ${CHANGE_AUTHOR_DISPLAY_NAME}"
    echo "CHANGE_AUTHOR_EMAIL: ${CHANGE_AUTHOR_EMAIL}"

}