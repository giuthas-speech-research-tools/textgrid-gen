# Install textgrid-gen

There's two main methods: Use either pip or uv. 

NOTE: Which ever you use, please note that `tggen`'s Python package name is
`textgrid-gen`. When installing from PyPi (with pip or uv or some other tool)
you will need to use this long name. There might a different package on PyPi
with the name tggen and installing that will not get you the right package.

## Using pip

This will work as soon as `textgrid-gen` is on pypi. 

## Using uv

There are other more programming oriented ways of running a package like
`textgrid-gen` with uv, but the following assumes the aim is to have a ordinary
command line command installed for ease of use.

Also of note is that the current way is just a hack as it is. See
[below](#when-pypi-is-available).

1. Get [uv](https://docs.astral.sh/uv/getting-started/installation/)
    - If you have no specific preference for install method, use the first system
      appropriate one from the linked page.
2. Get the `textgrid-gen` sources. Here are alternative ways of doing that:
   - Download and unpack them from
      [GitHub](https://github.com/giuthas-speech-research-tools/textgrid-gen/releases), or
   - clone the repository with ´git clone
      https://github.com/giuthas-speech-research-tools/textgrid-gen/´, 
   - or clone your own fork if you have forked `textgrid-gen`.
3. In the (unpacked) source directory run `uv tool install .` This will install two
   command line commands: `tggen` and `textgrid-gen`. The
   name of the installed package is computer-assisted-segmentation-tools.
4. See `tggen --help` for help and `tggen [command] --help` for more specific
   instructions and the documentation for even more.

If you need to upgrade `textgrid-gen`, first obtain updated sources (or edit
them yourself), then run `uv tool upgrade textgrid-gen --reinstall` in the same
directory. The `--reinstall` will be needed if the version number or
dependencies didn't update -- a usual case for needing this is making some
changes in the code and wanting to test them out.

### When PyPi is available

Once `textgrid-gen` is on PyPi, you can skip from step 1 to just running `uv
tool install computer-assisted-segmentation-tools`.  Upgrading to latest PyPi
version will also simplify to just running `uv tool upgrade textgrid-gen`.

If you do a PyPi install and want to test local code do it with `uv run textgrid-gen`.
If you only require an installation to test local code and want to use the short
`tggen` instead of `uv run tggen`, use the [above](Installing.markdown#using-uv)
instructions.
