node (){
  stage "checkout"
  git url: "https://github.com/robbyrussell/oh-my-zsh.git"
  stage "cat file"
  sh 'cat README.md'
  stage "another checkout!"
  git url: "https://github.com/lastpass/lastpass-cli.git"
  archive: "lpass.1.txt"
  stash includes: 'lpass.1.txt', name: 'text-file'
  stage "clear everything"
  sh 'rm -rf ${WORKSPACE}'
  stage "unstash and cat file"
  unstash 'text-file'
  sh 'cat lpass.1.txt'
  parallel (
    phase1: {
        label "phase1"
        sh "echo phase1"
    },
    phase2: {
        label "phase2"
        sh "echo phase2"
    }
  )
}

