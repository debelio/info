## Zypper

### The defaul package manager on SUSE and OpenSUSE Linux

| **command**                                                    | **explanation**                                       |
| :------------------------------------------------------------- | :---------------------------------------------------- |
| zypper install (in) git                                        | installing a package                                  |
| zypper install (in) git-3.5.0-7.x86_64.rpm                     | installing local package                              |
| zypper download nmap                                           | downloading package (/var/cache/zypp/packages/)       |
| zypper repos (lr) -u                                           | available repo                                        |
| zypper lr -d                                                   | detailed repo information                             |
| zypper lr -p                                                   | repo priorities                                       |
| zypper addrepo (ar) <options> <URI> <alias>                    | add a repo                                            |
| zypper ar <Path-to-Dir> <Name-of-Repository>                   | local repo                                            |
| zypper refresh (ref)                                           | update the repos                                      |
| zypper ref -s                                                  | refresh services as well as repos                     |
| zypper modifyrepo (mr) --disable (-d) 6                        | modify repo                                           |
| zypper namerepo (nr) 6 primary                                 | rename repo                                           |
| zypper removerepo (rr) main                                    | remove repo                                           |
| zypper rr -l                                                   | remove local repos                                    |
| zypper rr -t                                                   | remove all repos                                      |
| zypper search (se) nmap                                        | search for a package                                  |
| zypper se -i nmap                                              | search for installed package                          |
| zypper se -i                                                   | list all installed packages                           |
| zypper info (if) nmap                                          | info about a package                                  |
| zypper if -s nma                                               | info about a package by not knowing the exact name    |
| zypper in 'gcc<5.1'                                            | installing package by version (less than 5.1)         |
| zypper in gcc48-4.8.3+r212056-2.2.4                            | installing package by version (exactly this version)  |
| zypper in nfs\*                                                | install package by pattern                            |
| zypper info -t pattern lamp_server                             | get information about a pattern                       |
| zypper in amarok upd:libxine1                                  | install package from specific repo (using repo alias) |
| zypper in nmap main                                            | install package from specific repo (using main repo)  |
| zypper in nano -vi                                             | install one package, remove another in one go         |
| zypper rm apache2                                              | remove a package                                      |
| zypper rm -t pattern file_server                               | remove all files from the pattern                     |
| zypper rm -u apache2                                           | remove a package and all hist deps                    |
| zypper up                                                      | update system                                         |
| zypper dup                                                     | upgrade system                                        |
| zypper si mariadb                                              | install source and build deps                         |
| zypper in -D mariadb                                           | install only source for a package                     |
| zypper si -d mariadb                                           | install only build deps                               |
| zypper --quiet in mariadb                                      | install a package quietly                             |
| zypper –quiet rm apache2                                       | remove a package quietly                              |
| zypper mr -p 100 repo-oss                                      | set custom priority for a repo                        |
| zypper mr -ka                                                  | enable rpm file caching                               |
| zypper mr -ka repo-non-oss                                     | enable rpm file caching for a specific repo           |
| zypper mr -kt                                                  | enable rpm file caching for remote repos only         |
| zypper in -f --oldpackage flash-player-gnome=11.2.202.233-15.1 | downgrade a package                                   |
| zypper lu -a                                                   | list all available updates                            |
| zypper lu -r repo-oss                                          | list all available updates from a specific repo       |
| zypper lp                                                      | view available patches                                |
| zypper patch                                                   | install patches                                       |
| zypper patch -D                                                | dry-run patches install                               |
| zypper --non-interactive in -y nmap                            | use zypper install in scripts                         |
| zypper remove --no-confirm vim                                 | use zypper remove in scripts                          |
| zypper ve --details                                            | verify deps with details                              |
| zypper patch --updatestack-only                                | patch only zypper                                     |
| zypper packages --orphaned                                     | view orphaned packages                                |
| zypper ps                                                      | processes that are using deleted diles                |
| zypper what-provides 'perl(SVN::Core)'                         | searching packages by capabilities                    |
| zypper if --requires MozillaFirefox                            | viewing required/recommended modules                  |
| zypper sh                                                      | open zypper shell                                     |
| zypper -x                                                      | xml output                                            |
| zypper cc                                                      | clean the cache                                       |
| zypper lr --export backups/repos/foo.repo                      | export the repos                                      |
| zypper ar backups/repos/foo.repo                               | import the repos                                      |
| zypper ll                                                      | view locked packages                                  |
| zypper al MozillaFirefox                                       | add a package lock                                    |
| zypper rl MozillaFirefox                                       | remove a package lock                                 |

