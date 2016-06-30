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

}

