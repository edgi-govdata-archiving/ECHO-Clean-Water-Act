 [![Code of Conduct](https://img.shields.io/badge/%E2%9D%A4-code%20of%20conduct-blue.svg?style=flat)](https://github.com/edgi-govdata-archiving/overview/blob/master/CONDUCT.md)

# ECHO-Clean-Air-Act
This **archived** repo is home to a project exploring reported violations of the Clean Air Act. The project involves a Jupyter Notebook that interfaces with EPA's ECHO enforcement and compliance history database.

# Links to Notebooks

[echo-cwa-compliance-violations](https://colab.research.google.com/github/edgi-govdata-archiving/ECHO-Clean-Water-Act/blob/master/echo-cwa-compliance-violations.ipynb)

[CWA_Inspections](https://colab.research.google.com/github/edgi-govdata-archiving/ECHO-Clean-Water-Act/blob/master/echo-cwa-compliances-inspections.ipynb)

[CWA_Enforcements.ipynb](https://colab.research.google.com/github/edgi-govdata-archiving/ECHO-Clean-Water-Act/blob/master/echo-cwa-enforcements.ipynb)

# Default branch - 'main'
The 'master' branch is no longer the repo's primary branch in line with EDGI's policy decided here: https://github.com/edgi-govdata-archiving/overview/issues/241

> If someone has a local clone, they can update their locals like this:
```
$ git checkout master
$ git branch -m master main
$ git fetch
$ git branch --unset-upstream
$ git branch -u origin/main
$ git symbolic-ref refs/remotes/origin/HEAD refs/remotes/origin/main
```
> The above steps accomplish:
> - Go to the master branch
> - Rename master to main locally
> - Get the latest commits from the server
> - Remove the link to origin/master
> - Add a link to origin/main
> - Update the default branch to be origin/main

(From @jywarren at Public Lab: https://github.com/publiclab/plots2/issues/8077)


## License & Copyright

Copyright (C) <year> Environmental Data and Governance Initiative (EDGI)
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, version 3.0.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

See the [`LICENSE`](/LICENSE) file for details.
