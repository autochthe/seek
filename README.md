# patterns-shell

**patterns-shell** - Design patterns for shell scripts


## Installation

You can manually copy this repository, but it is better to clone it via `git` with

>git clone https://github.com/resultsreturned/patterns-shell.git

Then you can easily get updates with

>git pull


## Patterns

### Scripts
* *autoscreen* - auto start a GNU screen session without inception
* *pgdb* - manage PostgreSQL databases
* *remote* - manage connections via SSH and SCP
* *untar* - untar and unzip archives

For detailed descriptions of these scripts,  
see `scripts/README.md`

### Templates

You can use templates to generate code.  Several scripts include
template-\* functions.  These functions take arguments and generate shell scripts
based off templates. You can save this output, analyze it, and source it, or you
can source it directly with process substitution:

>source &lt;(template-\* arg1 arg2 ... argn)

All generated functions are self documenting.  You can view this documentation with

>funcname -h

The template functions are listed below:

* **pgdb**
    * *template-db* - Generate function to access a database as a user
    * *template-dbbackup* - Generate function to backup and restore a database
* **remote**
    * *template-remote* - Generate functions to connect to a server via SSH, and push/pull files via SCP
* **sourcedir**
    * *template-sourcedir* - Generate script to source all files in a directory
        * NOTE: this template function does not behave correctly in process substitution  
          Save the output to a file and source that instead

For detailed descriptions of these functions and the code they generate,  
see `templates/README.md`

## License

patterns-shell

Copyright (C) 2013  Mara Kim

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
