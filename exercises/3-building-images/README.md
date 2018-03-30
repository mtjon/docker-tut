# Building Images
At some point, using (publicly) available, existing images won't suffice your uses. At this point you'll want to build your own images. These are defined by a `Dockerfile` and built using the `docker build` command.

## Structure
Every image you build needs to inherit from an existing image, e.g. `ubuntu`, or `jupyter/base-notebook`.

An example Dockerfile can be found in this directory.

## Exercise
Let's build something somewhat relevant: a redis-enabled jupyter notebook image.
Instructions:
- Base it off jupyter's `jupyter/datascience-notebook`, choose a specific tag: `2c80cf3537ca`
- install the redis packages using the `conda` environment manager:
    - `redis-py`
- Clean your cache after installation to minimize image size.
- Jupyter's images come with a `fix-permissions.sh`-script to fix permissions after installation, this needs to be run using:
    - fix-permissions $DIRECTORY ($HOME_DIR will suffice in this case)
- After installing; change the working directory to `$HOME/work/`

## Pointers
- You *always* need a `FROM image[:tag]` at the top of your Dockerfile.
- Be aware of the order in which you run commands, every command is stored as a separate layer in the image.
- When using `RUN` in your Dockerfile, you may use `&&` to run the next command upon succesfully running the previous (as opposed to `;`, which will run the next command regardless).
    - Concatenate multiple related commands into a single image layer to prevent exploding the image.
- When building an image, you cannot manually enter prompots; installs need to be automatically accepted, e.g. for `conda install`, add the `-y`-flag.
- You may choose to name your `Dockerfile` differently, but then you'll have to manually point `docker build` to the file.
- `jupyter/*-notebook` expose port 8888, this can be published in your `docker run`