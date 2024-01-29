Not sure why there's a rebuild on `nix run -- watch .`

Partly to do with trusted-substituters and trusted-users as discussed at

https://github.com/NixOS/nix/issues/8248
https://github.com/NixOS/nix/issues/9649#issuecomment-1868001568
https://github.com/NixOS/nix/issues/6672

Not sure why the whole thing isn't cached though, since it seems I
often have to rebuild when I haven't done so in a while with no
changes to `flake.lock`.

Partial solution seems to be to: `sudo nix run` once to cache what needs
to be.
