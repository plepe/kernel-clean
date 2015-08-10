Script to remove all installed kernels but the newest one and the currently running.

Installation
============
```sh
cd /usr/local
git clone https://github.com/plepe/kernel-clean.git
ln -s /usr/local/kernel-clean/kernel-clean /usr/local/bin/
```

Execution
=========
Run `kernel-clean` to remove old kernels.
You can add the `-y` command line option which gets passed to
`apt-get` and means "Assume Yes to all queries and do not prompt".

Automation
==========
One way to automate the clean up is by executing `kernel-clean -y`
automatically by cron every once in a while, for example once per week:
`ln -s /usr/local/kernel-clean/kernel-clean.hook /etc/cron.weekly/kernel-clean`

Contributors
============
* Stephan Bösch-Plepelits @plepe
* Stefan Tauner @stefanct
