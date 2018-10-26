## Minified Docker image with Python and Java

Basic [Docker](https://www.docker.com/) image to run [Python](https://www.python.org/) and [Java](https://www.java.com/) applications.
This image is:
- Based on [python/2.7.15-alphine3.7](https://github.com/docker-library/python/blob/ac49e0bb09aafe4100fe5662636c24fce7206008/2.7/alpine3.7/Dockerfile)
- With generation script forked and modified from [anapsix/alpine-java](https://github.com/anapsix/docker-alpine-java)

### Versions/tags

| software     | version      |
|--------------|--------------|
| alpine       | `3.7`        |
| python       | `2.7.15`     |
| glibc        | `2.28-r0`    |
| java 8       | `8u192b12`   |

#### MAJOR TAGGING UPDATE
To allow selection of specific Java version, a **major retagging is taking place**.
Old tags will remain for compatibility sake, but are no longer documented.
`:8`,`:7` and `:latest` are all valid, but are not "locked" to any specific Java version / patch set - i.e. depending on when you pull the `:8` tagged image, for example, you might end up with `8u102b14`, `8u112b15`, `8u121b13`, etc..
Well, `:7` no as much, since it's EOL and no more patches are released.

However specific `:8uXXXbYY` tags (such as `:8u102b14`, `:8u112b15`) will guarantee particular MAJOR-MINOR-BUILD Java versions.

Specific version tagging is manually done, no guarantee that all minor builds will be covered.

#### JCE Policy
Special `_unlimited` images are available with Unlimited JCE Policy

**Latest JRE8/JDK8 Version**: `8u192b12`

### Tags

Latest Oracle Java 8 Server-JRE:
* `latest`
* `8`
* `8_server-jre`
* `8_server-jre_unlimited`

Latest Oracle Java 8 JDK (plus DCEVM variant)
* `8_jdk`
* `8_jdk_unlimited`
* `8_jdk-dcevm`
* `8_jdk-dcevm_unlimited`


### Usage

Example:

    docker run -it --rm alpine-python-java python

    docker run -it --rm alpine-python-java java -version

### Disclaimer

By using Dockerfiles contained in this repo and/or container images derived from them, you are agreeing to any and all applicable software licences, license agreements & export rules related to unlimited strength crypto, etc..
