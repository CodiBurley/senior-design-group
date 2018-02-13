# Notes

This is a collection of notes I've taken throughout my experience with the senior design
project on a MacBook Pro. Following http://blog.japaric.io/quickstart/ and
https://docs.rs/cortex-m-quickstart/0.2.0/cortex_m_quickstart/.

# Dependencies

### Installing `xargo`

Ran `cargo install xargo`

### Installing `OpenOCD`

Ran `brew install openocd`

### Installing GCC ARM toolchain

Ran `brew install caskroom/cask/gcc-arm-embedded` which I got from
https://gist.github.com/joegoggins/7763637#gistcomment-1250738. This yielded the following:

```
==> Tapping caskroom/cask
Cloning into '/usr/local/Homebrew/Library/Taps/caskroom/homebrew-cask'...
remote: Counting objects: 4013, done.
remote: Compressing objects: 100% (3986/3986), done.
remote: Total 4013 (delta 34), reused 530 (delta 23), pack-reused 0
Receiving objects: 100% (4013/4013), 1.37 MiB | 5.06 MiB/s, done.
Resolving deltas: 100% (34/34), done.
Tapped 0 formulae (4,022 files, 4.3MB)
==> brew cask install caskroom/cask/gcc-arm-embedded 
==> Creating Caskroom at /usr/local/Caskroom
==> We'll set permissions properly so we won't need sudo in the future
Password:
==> Satisfying dependencies
==> Downloading https://developer.arm.com/-/media/Files/downloads/gnu-rm/7-2017q4/gcc-arm-none-eabi-7-2017-q4-major-mac.tar.bz2
######################################################################## 100.0%
==> Verifying checksum for Cask gcc-arm-embedded
==> Installing Cask gcc-arm-embedded
==> Linking Binary 'arm-none-eabi-strip' to '/usr/local/bin/arm-none-eabi-strip'.
==> Linking Binary 'arm-none-eabi-ar' to '/usr/local/bin/arm-none-eabi-ar'.
==> Linking Binary 'arm-none-eabi-as' to '/usr/local/bin/arm-none-eabi-as'.
==> Linking Binary 'arm-none-eabi-c++' to '/usr/local/bin/arm-none-eabi-c++'.
==> Linking Binary 'arm-none-eabi-c++filt' to '/usr/local/bin/arm-none-eabi-c++filt'.
==> Linking Binary 'arm-none-eabi-cpp' to '/usr/local/bin/arm-none-eabi-cpp'.
==> Linking Binary 'arm-none-eabi-elfedit' to '/usr/local/bin/arm-none-eabi-elfedit'.
==> Linking Binary 'arm-none-eabi-g++' to '/usr/local/bin/arm-none-eabi-g++'.
==> Linking Binary 'arm-none-eabi-gcc' to '/usr/local/bin/arm-none-eabi-gcc'.
==> Linking Binary 'arm-none-eabi-gcc-ar' to '/usr/local/bin/arm-none-eabi-gcc-ar'.
==> Linking Binary 'arm-none-eabi-gcc-nm' to '/usr/local/bin/arm-none-eabi-gcc-nm'.
==> Linking Binary 'arm-none-eabi-gcc-ranlib' to '/usr/local/bin/arm-none-eabi-gcc-ranlib'.
==> Linking Binary 'arm-none-eabi-gcov' to '/usr/local/bin/arm-none-eabi-gcov'.
==> Linking Binary 'arm-none-eabi-gcov-tool' to '/usr/local/bin/arm-none-eabi-gcov-tool'.
==> Linking Binary 'arm-none-eabi-gdb' to '/usr/local/bin/arm-none-eabi-gdb'.
==> Linking Binary 'arm-none-eabi-gdb-py' to '/usr/local/bin/arm-none-eabi-gdb-py'.
==> Linking Binary 'arm-none-eabi-gprof' to '/usr/local/bin/arm-none-eabi-gprof'.
==> Linking Binary 'arm-none-eabi-ld' to '/usr/local/bin/arm-none-eabi-ld'.
==> Linking Binary 'arm-none-eabi-ld.bfd' to '/usr/local/bin/arm-none-eabi-ld.bfd'.
==> Linking Binary 'arm-none-eabi-nm' to '/usr/local/bin/arm-none-eabi-nm'.
==> Linking Binary 'arm-none-eabi-objcopy' to '/usr/local/bin/arm-none-eabi-objcopy'.
==> Linking Binary 'arm-none-eabi-objdump' to '/usr/local/bin/arm-none-eabi-objdump'.
==> Linking Binary 'arm-none-eabi-ranlib' to '/usr/local/bin/arm-none-eabi-ranlib'.
==> Linking Binary 'arm-none-eabi-readelf' to '/usr/local/bin/arm-none-eabi-readelf'.
==> Linking Binary 'arm-none-eabi-size' to '/usr/local/bin/arm-none-eabi-size'.
==> Linking Binary 'arm-none-eabi-strings' to '/usr/local/bin/arm-none-eabi-strings'.
==> Linking Binary 'arm-none-eabi-addr2line' to '/usr/local/bin/arm-none-eabi-addr2line'.
🍺  gcc-arm-embedded was successfully installed!
```

# Running

```sh
xargo build --example hello
```

This yielded an error, which was solvable by:

```sh
rustup component add rust-src
```

Which got me one step further...I'm now seeing

```
error: linking with `arm-none-eabi-gcc` failed: exit code: 1
```
