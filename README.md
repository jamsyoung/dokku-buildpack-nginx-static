# Dokku Buildpack: Static Nginx With Custom Root
This is basically a clone of numerous static Nginx buildpacks out there with
the added benefit of allowing the project root to be set in an environment
variable so your project is not forced to put the root of the static site you
are serving in a specific location that may not be ideal for what you are
doing.


## How to add
In your repository create a `.env` file containing the following:

```
export BUILDPACK_URL="https://github.com/jamsyoung/dokku-buildpack-nginx-static.git"
```

Also create a directory named `.profile.d`.  Inside of that directory add a file
named `startup.sh`.  This can actually be named anything, as long as it ends in
`.sh`, as far as I know.  Inside this file, set the location to your
`index.html` relative to your project root.  For most of my projects this is in
`public`.

```
export PROJECT_ROOT=public
```
