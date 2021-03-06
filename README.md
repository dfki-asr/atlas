ATLAS
=====

ATLAS (which stands for "Advanced Three-dimensional Large-scale Asset Server") is a system for
storage and conversion of polygonal 3D models. It offers a REST interface to add and retrieve
models, where HTTP content negotiation is used to determine the input and output format(s).

Its current primary use is to import 3D models into its own storage format, and export them
to something usable on the web.


Repository structure
--------------------

This repository binds together the components required to build and run ATLAS, as a sort of "convenience" repository.
It's intended to be kept in a state where cloning and building from it will give you the most recent, stable, ATLAS.

However, this means you will need to use

    git clone --recursive

when cloning this repository, since it references the other atlas repositories as submodules.
If you've already cloned this repository without the `--recursive` flag, you need to manually download and setup the submodules by running

    git submodule update --init --recursive

in the cloned repositories directory.


Building
--------

You need a JDK (Java 7 or newer, tested with Oracle JDK) and Maven (version 3 upwards) to build the Java part.
Getting those installed for your operating system is left as an exercise to the reader.
Once these build prerequisites are in place, you should just be able to say

    mvn install 

from this directory (with `README` and `pom.xml`), and an `atlas-[version].war` should be built in the `atlas-server` submodule.

You also need to build the import worker, see the [worker README](https://github.com/dfki-asr/atlas-worker/blob/master/README.md) for details.


Running
-------

See the [server README](https://github.com/dfki-asr/atlas-server/blob/master/README.md) and [worker README](https://github.com/dfki-asr/atlas-worker/blob/master/README.md) for details.


Contributing
------------

Contributions are very welcome. However, it makes much more sense to contribute to the repositories linked from here.


License
-------

Our code (and documentation) is licensed under the Apache License version 2.0. You should have received an approriate LICENSE.txt file with this distribution. At any rate, you can get the official license text from http://www.apache.org/licenses/LICENSE-2.0.txt

