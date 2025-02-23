# Overworld Client v1.1

## About
This Godot 4.x plugin will allow your Godot applications to download and update the
latest & greatest client bindings from your own [Overworld](https://github.com/saltysystems/overworld) server.

![Plugins](/gh-images/download-compile.png)

## Usage

1. Open your Godot project, or use an existing one.
2. Copy the `addons` directory from this repository to your project
3. Click `Project`, then `Project Settings`.
4. Choose the `Plugins` tab, and set the OverworldClient plugin to `Active`

![Enable](/gh-images/enable-plugin.png)

At this point, the Overworld client panel will appear in Godot. 

You will want to add your server address, e.g. 
```
http://address.of.your.server:<port>/client/download
```

The `/client/download` route is the standard route for autogenerated Overworld
zip files.

Next, you'll want to create or select an output directory. By default, Overworld
assumes that you will put scripts in `res://scripts`. 

Once Overworld compiles your client libraries, it will delete the intermediate
format `.proto` files downloaded from the server. You keep these files if you
wish by selecting `Do not delete .proto files`. However, they are not directly
used by any Overworld client library.
