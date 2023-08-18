# ansible-desktop

## Pre-requisites

1. If on Mac, install Homebrew and Ansible 
2. Clone this repo and move into it


## Setting up the script

The instructions and inspiration for this is taken from: 
https://opensource.com/article/22/6/install-software-macos-ansible-homebrew

1. Install ansible 
  
  ```sh
  brew install ansible  
  ```

2. Run this in your terminal

  ```sh
  cat << EOF >> inventory
  [localhost\]
  your-host-name
  EOF
  ```

3. Create a ansible playbook
