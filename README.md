[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FAten2k%2Fcookiecutter-etna-c.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FAten2k%2Fcookiecutter-etna-c?ref=badge_shield)

cookiecutter-etna-c
===========

`cookiecutter-etna-c` is a template for simple projects written in C with
autotools.

Usage
-----

You need [cookiecutter][], a tool to create projects from project
templates. Once installed (in a virtualenv or just with `pip install
cookiecutter`), you can use the following command:

    cookiecutter https://github.com/aten2k/cookiecutter-etna-c.git
    cd your-project
    git init
    git add .
    git commit -m "Initial commit"

[cookiecutter]: https://github.com/audreyr/cookiecutter

Then, use the following command to get the first steps to get started:

    git ls-tree -r --name-only HEAD | \
          xargs grep -nH "T[O]DO:" | \
          sed 's/\([^:]*:[^:]*\):\(.*\)T[O]DO:\(.*\)/\3 (\1)/' | \
          sort -ns | \
          awk '(last != $1) {print ""} {last=$1 ; print}'

Once you are done, your project is ready and you can compile it with
and get a release tarball with:

    sh autogen.sh
    mkdir build
    cd build
    ../configure
    make
    make dist

Once you want to make a release, tag the tree with `git tag 1.3`, then
run the previous commands from the top. You'll get a properly
versioned tarball with a `ChangeLog` file if this is not your first
version.


## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FAten2k%2Fcookiecutter-etna-c.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FAten2k%2Fcookiecutter-etna-c?ref=badge_large)