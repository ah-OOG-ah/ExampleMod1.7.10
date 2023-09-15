# Example Forge Mod for Minecraft 1.7.10

no status buttons 4 u

A fork of GTNH's Example mod, for when I don't want to wait for them to add features.

### Help! I'm stuck!

For the forseeable future, go use GTNH's version or figure it out yourself. This is not intended for anyone else to
seriously use.

### Files
 - [`build.gradle`](https://github.com/GTNewHorizons/ExampleMod1.7.10/blob/main/build.gradle): This is the core script of the build process. You should not need to tamper with it, unless you are trying to accomplish something out of the ordinary. __Do not touch this file! You will make a future update near impossible if you do so!__
 - [`gradle.properties`](https://github.com/GTNewHorizons/ExampleMod1.7.10/blob/main/gradle.properties): The core configuration file. It includes
 - [`dependencies.gradle[.kts]`](https://github.com/GTNewHorizons/ExampleMod1.7.10/blob/main/dependencies.gradle): Add your mod's dependencies in this file. This is separate from the main build script, so you may replace the [`build.gradle`](https://github.com/SinTh0r4s/ExampleMod1.7.10/blob/main/build.gradle) if an update is available.
 - [`repositories.gradle[.kts]`](https://github.com/GTNewHorizons/ExampleMod1.7.10/blob/main/repositories.gradle): Add your dependencies' repositories. This is separate from the main build script, so you may replace the [`build.gradle`](https://github.com/SinTh0r4s/ExampleMod1.7.10/blob/main/build.gradle) if an update is available.
 - [`jitpack.yml`](https://github.com/GTNewHorizons/ExampleMod1.7.10/blob/main/jitpack.yml): Ensures that your mod is available as import over [Jitpack](https://jitpack.io).
 - [`.github/workflows/gradle.yml`](https://github.com/GTNewHorizons/ExampleMod1.7.10/blob/main/.github/workflows/gradle.yml): A simple CI script that will build your mod any time it is pushed to `master` or `main` and publish the result as release in your repository. This feature is free with GitHub if your repository is public.

### Forge's Access Transformers

You may activate Forge's Access Transformers by defining a configuration file in `gradle.properties`.

Check out the [`example-access-transformers`](https://github.com/GTNewHorizons/ExampleMod1.7.10/tree/example-access-transformers) brach for a working example!

__Warning:__ Access Transformers are bugged and will deny you any sources for the decompiled minecraft! Your development environment will still work, but you might face some inconveniences. For example, IntelliJ will not permit searches in dependencies without attached sources.

### Mixins

Mixins are usually used to modify vanilla or mod/library in runtime without having to change source code. For example, redirect a call, change visibility or make class implement your interface. It's an advanced topic and most mods don't need to do that.

You can activate Mixin in 'gradle.properties'. In that case a mixin configuration (usually named `mixins.mymodid.json`) will be generated automatically, and you only have to write the mixins itself. Dependencies are handled as well.
Take a look at the examples in [Hodgepodge](https://github.com/GTNewHorizons/Hodgepodge/) and [Angelica](https://github.com/GTNewHorizons/Angelica/pull/8).

### Advanced

If your project requires custom gradle commands you may add a `addon.gradle[.kts]` to your project. It will be added automatically to the build script. Although we recommend against it, it is sometimes required. When in doubt, feel free to ask us about it. You may break future updates of this build system!
If you need access to properties modified later in the buildscript, you can also use a `addon.late.gradle[.kts]`.
For local tweaks that you don't want to commit to Git, like adding extra JVM arguments for testing, use `addon[.late].local.gradle[.kts]`.

### Feedback wanted

If you tried out this build script we would love to head your opinion! Is there any feature missing for you? Did something not work? Please open an issue and we will try to resolve it asap!

Happy modding, \
[SinTh0r4s](https://github.com/SinTh0r4s), [TheElan](https://github.com/TheElan) and [basdxz](https://github.com/basdxz)
