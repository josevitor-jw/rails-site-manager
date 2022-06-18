```
Roberto Nogueira  
BSd EE, MSd CE
Solution Integrator Experienced - Certified by Ericsson
```

# Rails Site Manager

![project image](images/project.png)

**About**

This is in order to help the working CLI daily activities. It shows live relevant rails project information in the cli such as `rvm`, `env`, `db` and `git` domains, `services` and `databases` information.

**Advantages:**

* Development Flux and Environment seamlessly integrated.
* Live `rvm`, `env`, `db` and `git` domains, `services` and `databases` information.
* Support local and remote databases setups, remote import and download databases.
* Support start/stop services at once with consolidated logs.
* Better db consoles for `mysql`, `postgresql` and `redis`.

Dependences:

* Packages: ansi, iredis, mycli, pgcli, pv and wget.
* Gem: foreman.

See example of use below:

![](images/screenshot1.png)

## Requirements and Tips

In order to install `Site Manager`, it is required that the following has been installed already:

* [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* [project-today-manager](https://github.com/enogrob/project-today-manager)
* [project-tag-manager](https://github.com/enogrob/project-tag-manager)

**For further help:**

```shell
Crafted (c) 2021~22 by Encora - We are stronger together
Site v1.0.00

site    [print|version]
::
rvm.domain    [print]
env.domain    [print|development|test]
dbs.domain    [print|local|remote|multi]
git.domain    [print|encora|gmail]
::
dbs    [print|download|import|dumps]
services    [print|start|stop]
::
homepage https://github.com/enogrob/rails-site-manager
```

**Installation:**

```
pushd /tmp
# install site
mkdir -p ~/Projects
cd ~/Projects
git clone git@github.com:enogrob/rails-site-manager.git
echo "test -f ~/Projects/rails-site-manager/site && source ~/Projects/rails-site-manager/site" >> ~/.bashrc
source ~/.bashrc
# install site deps
curl -OL git.io/ansi
chmod 755 ansi
sudo mv ansi /usr/local/bin/
brew bundle Brewfile
gem install foreman --no-document
popd
```

**Configuration**

It is required that the initial values for `domains` are set in initialization section of the `site` script e.g. `site.init`. Also the Puppet credentials has to be setup in the `~/.bashrc` .

**Changes log**

* **1.0.01** First release.

**Refs:**

* ansi
* foreman
* iredis
* mycli
* pgcli
* pv
* wget
