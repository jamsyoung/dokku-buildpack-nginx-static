# Dokku buildpack: Static Nginx With Custom Root
This is basically a clone of numerous static Nginx buildpacks out there with
the added benefit of allowing the project root to be set in an environment
variable so your project is not forced to put the root of the static site you
are serving in a specific location that may not be ideal for what you are
doing.


## How to add
In your repository create a `.env` file containing the following.  Set the
PROEJCT_ROOT to be whatever you need it to be.

```
export PROJECT_ROOT=public
export BUILDPACK_URL="https://github.com/jamsyoung/dokku-buildpack-nginx-static.git"
```
