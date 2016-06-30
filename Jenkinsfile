node (){
  stage "checkout"
  git url: "https://github.com/robbyrussell/oh-my-zsh.git"
  stage "cat file"
  sh 'cat README.md'
  stage "anothe checkout!"
  git url: "https://github.com/lastpass/lastpass-cli.git"
  archive: "lpass.1.txt"
}

