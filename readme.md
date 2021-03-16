# 🐓 Chicken package

## About

* * *

Please add relevant information about your package.

## Tooling information

* * *

Targeted audience we are building for is Windows 10, MacOSX and Linux users. This
project uses [Meson](https://mesonbuild.com/) `0.57.1` and newer.

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

You may find that I have a number of ways that you can contact
me. All of these methods happen to be listed on my blogging platform
[Mike's virtual office](https://michaelbrockus.home.blog/contact/).

Lastly don't forget to have a cup of virtual coffee. Thanks.
