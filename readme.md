# 🐓 Chicken package

## About

* * *

Please add relevant information about your package.

## Tooling information

* * *

Targeted audience we are building for is Windows 10, MacOSX and Linux users. This
project uses [Meson](https://mesonbuild.com/) `0.56.0` and newer.

## Setup, Compile and Install

* * *

Using this package should be fairly simple just add the git wrap file in your subprojects
directory and include the dependency in your project.

```console
[wrap-git]
directory = chicken
url = https://github.com/chicken-libraries/chicken.git
revision = main

[provide]
chicken = chicken_dep
```


The next step should be to add the package to your Meson project:

```meson
chicken_dep = dependency('chicken')

executable('prog', files('main.c'),
    dependencies : [chicken_dep])

```

And finally we setup, and compile the project just like normal.

## Usage of this package

* * *

Here is a simple sample application that should get you up and running with using this
library as soon as possible but to learn more please view the API documentation thanks.

```c
#include <stdio.h>
#include <stdlib.h>
#include <chicken/package.h>

//
// main is where all good examples start
//
int main(void)
{
    puts(greet());
    return EXIT_SUCCESS;
} // end of function main

```

## Contact the developers

* * *

You might want to visit the [Chicken Libraries website](https://chickenlibraries.wordpress.com/)
for more information on the organization along with the documentation.
