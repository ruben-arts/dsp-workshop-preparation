# Prefix.dev <> DSP/EY Workshop Preparation Example
To test if the most improtant dependencies are reachable on your machines you could run this example in your network.

It will test the following:
- Pixi installation
- Prefix.dev server access
- GitHub Access
- PyPI access
- Anaconda access

We can easily get rid of the Anaconda access by replacing `"bioconda"` with `"https://prefix.dev/bioconda"` in the `pixi.toml` file.

# Testing
Have `pixi` installed and accessible in the terminal.
This can be done through the [Pixi installation documentation](https://pixi.sh/latest/installation/).

Then please run the following:
```
# Clone this repo
git clone https://github.com/your/repo.git

# Change to the directory
cd repo

# Install all environments
pixi install --all
```
This should succeed without any errors.

Afterwards lets test the result without a lockfile:
```
rm pixi.lock
pixi install --all
```
If this succeeds, you have a working Pixi installation and access to the required resources.

# Testing Docker
If you have Docker installed, you can also test the Docker image:
```
docker run --rm -it ghcr.io/prefix-dev/pixi:0.48.0 pixi --version
```
Resulting in:
```bash
# Docker output....
pixi 0.48.0
```

