# ubuntu

> Usefull information about ubuntu disributive

- Print installed packages
`dpkg-query -l`

- Show files inside package
`dpkg-query -L {{package}}`

- Search packet by name
`apt-cache search {{name}}`

- Display ubuntu version
`lsb_release -a`

- Show list of packages in repository
`grep ^Package /var/lib/apt/lists/{{repository-name*_Packages}} | awk '{print $2}' | sort -u`
