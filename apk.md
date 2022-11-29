## Apk

### The default package manager on Alpine Linux

| **command**                                                    | **explanation**                                       |
| :------------------------------------------------------------- | :---------------------------------------------------- |
| apk update                                                     | update the package list                               |
| apk add vim                                                    | installing a package                                  |
| apk add --allow-untrusted vim-8.2.2137-r0.apk                  | installing a local package                            |
| apk del vim                                                    | remove an installed package                           |
| apk search -v                                                  | list all available packages in the repositories       |
| apk search -v 'vim*'                                           | search for a package using a pattern for the name     |
| apk search -v -d 'disk'                                        | search for a package using a pattern for the description |
| apk info vim                                                   | display the details of a specific package             |
| apk info -a vim                                                | display the details of a specific package and it's dependencies |
| apk info -vv                                                   | list all installed packages with the version and description |
| apk -U upgrade                                                 | upgraded all packages, updating the cache before that |
| apk add vim=8.2.0-r0 or apk add 'vim<8.2.1'                    | hold a package to a specific version                  |
| apk fetch vim                                                  | download a package                                    |
| apk fetch -R vim                                               | download a package with the requirements              |
| apk policy vim                                                 | display repository details of a package               |
| apk stats                                                      | show statistics of the packages and the repositories  |
| apk -v cache clean                                             | clean the package cache                               |
| apk cache download                                             | download deleted from the cache packages              |
