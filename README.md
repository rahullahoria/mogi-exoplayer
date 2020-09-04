# Mogi ExoPlayer #

## Step 1.

First, clone the repository into a local directory and checkout the desired
branch:

```sh
git clone https://github.com/rahullahoria/mogi-exoplayer.git

```

## Step 2. 
Next, add the following to your project's `settings.gradle` file, replacing
`path/to/exoplayer` with the path to your local copy:

```gradle
gradle.ext.exoplayerRoot = 'path/to/exoplayer'
gradle.ext.exoplayerModulePrefix = 'exoplayer-'
apply from: new File(gradle.ext.exoplayerRoot, 'core_settings.gradle')
```

## Step 3.
You should now see the ExoPlayer modules appear as part of your project. You can
depend on them as you would on any other local module, for example:

```gradle
implementation project(':exoplayer-library-core')
implementation project(':exoplayer-library-hls')
implementation project(':exoplayer-library-ui')
```


