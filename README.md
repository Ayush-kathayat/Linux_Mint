# Linux_Mint

# Things to do after install -

## Setup zsh

i. Install zsh
```.sh
  sudo apt install zsh
```
ii. Set zsh as default 
```.sh
  cat /etc/shells
  # check the path of zsh (probabally /usr/bin/zsh) 

  # changing the defafult terminal to zsh
  chsh
  # choose /usr/bin/zsh (or the path you found in previous step)

  cshsh -s /usr/bin/zsh
  # replace /usr/bin/zsh with the path you found
```
iii. Restart

iv. Run zsh4humans
```.sh
if command -v curl >/dev/null 2>&1; then
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/romkatv/zsh4humans/v5/install)"
else
  sh -c "$(wget -O- https://raw.githubusercontent.com/romkatv/zsh4humans/v5/install)"
fi
```
