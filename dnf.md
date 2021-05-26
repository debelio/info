## dnf

### The next generation version of _yum_

| **command**                                                                | **explanation**                             |
| :------------------------------------------------------------------------- | :------------------------------------------ |
| dnf install httpd                                                          | installing a package                        |
| dnf install httpd-manual -y                                                | install and assume "yes"                    |
| dnf check-update                                                           | check for available updates                 |
| dnf update bash -y                                                         | update a package                            |
| dnf install dnf-plugins-core && dnf download httpd                         | download package                            |
| dnf install unbound-1.4.20-28.el7.x86_64.rpm                               | install local package                       |
| dnf remove httpd                                                           | uninstall package                           |
| dnf reinstall httpd -y                                                     | reinstall package                           |
| dnf repolist all                                                           | view repo information                       |
| dnf config-manager --add-repo="https://mirror.aarnet.edu.au/pub/centos/7"  | add new repo                                |
| dnf --enablerepo=https://mirror.aarnet.edu.au/pub/centos/7 install neovim  | enable specific repo                        |
| dnf --disablerepo=https://mirror.aarnet.edu.au/pub/centos/7 install neovim | disable specific repo                       |
| dnf search php                                                             | search for a package                        |
| dnf provides \*/iscsiadm                                                   | find which package provides something       |
| dnf provides /etc/httpd/conf/httpd.conf                                    | find which package provides this local file |
| dnf info httpd                                                             | view package info                           |
| dnf history                                                                | view transaction history                    |
| dnf history info 13                                                        | view specific transaction history info      |
| dnf history undo 13 -y                                                     | undo specific transaction history           |
| dnf history redo 13 -y                                                     | redo specific transaction history           |
| dnf clean all                                                              | clear cache                                 |
| dnf makecache                                                              | build cache                                 |
| dnf list installed                                                         | list installed packages                     |
| dnf grouplist                                                              | list package groups                         |
| dnf groupinfo "Basic Web Server"                                           | info for a specific package group           |
| dnf groupinstall "Web Server" -y                                           | install a specific package group            |
| dnf update -x kernel                                                       | exclude a specific package                  |
| dnf updateinfo list sec                                                    | list security updates only                  |
| dnf install httpd -y -q                                                    | be quiet                                    |
| dnf remove httpd -y -v                                                     | display verbose info                        |
