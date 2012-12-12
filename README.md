# Introduction

Blueprint of strategies and plays

## Usage

First clone this repo

    $ git clone https://github.com/bluenerv/blueprint.git

Then init and update the submodules

    $ cd blueprint
    $ git submodule init
    $ git submodule update
    $ cd -

Next edit your global variables with the correct paths

    $ cp playbooks/global/vars/{templates,main}.yml
    $ vi playbooks/global/vars/main.yml

Now prepare your ansible environment (assumes you already have the proper python modules installed in accordance to ansible)

    $ cd ansible
    $ source ./hacking/env-setup
    $ cd -

Edit the hosts file and point at a test machine, otherwise you will apply the strategybook on localhost

    $ vi hosts

Finally you can now execute a strategybook

    $ ansible-playbook strategybooks/sandbox/play.yml
