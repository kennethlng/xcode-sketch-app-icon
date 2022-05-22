# How to Use Apple's App Icon Sketch Template for Xcode

Developing an app for iOS requires you to import your app icon in a variety of file sizes and resolutions to fit different needs. Fortunately, Apple’s Design Resources comes with free Sketch and Photoshop templates. All you have to do is plug in your SVG icon once and you’ll get the full set of files to import into Xcode.

First, download [Sketch](https://www.sketch.com/). You can get started with the 30-day free trial or pay for a one-year license.

![64BB7522-2A97-4002-80FD-A3DE902A1209](https://user-images.githubusercontent.com/13254616/169708168-09b0e292-e821-48cf-87f9-0eca16a073af.png)

Grab the app icon Sketch temlate from Apple's [Design Resources](https://developer.apple.com/design/resources/).

![885BCBA9-09C6-4F81-9673-465C26835BDA](https://user-images.githubusercontent.com/13254616/169708191-f1b28bbe-c12e-431e-ba1a-03094d7bd7c6.png)

Once you open the Sketch template, click on the “Template — App Icons” layer in the panel and you’ll see all the app icon sizes. Each app icon size is connected to the same symbol, so you only need to add your icon to the symbol and every layer will be automatically populated with your icon.

![C0A0DD7C-1B6B-4745-9746-0BC442675F77](https://user-images.githubusercontent.com/13254616/169708202-65aca4be-b089-4de3-91db-31ad3a9ed24e.png)

> A symbol in Sketch is a reusable component. Any changes made to the symbol is applied everywhere.

In the left panel under “LAYERS”, select Symbols.

![865592DE-2314-4586-B82E-7055E11587C1](https://user-images.githubusercontent.com/13254616/169708219-a9136faf-e5c8-47f2-a4d1-47cd5b2c4640.png)

You’ll see two symbols: “App Icon Square” and “App Icon Wide”. For this post, we’ll just focus on the “App Icon” symbol.

Drag your icon file into Sketch and onto the “App Icon Square” symbol. Make sure your icon is an SVG file. Modify it until it fits according to how you want it.

![0BD8A76F-6AF1-41E5-94FB-50A60EE88A6A](https://user-images.githubusercontent.com/13254616/169708246-e338d0e8-30b3-4e9b-8563-ec2fc33e86e6.png)

> If you don’t have an app icon yet, use a temporary one from [flaticon.com](https://www.flaticon.com/). They have tons of icons available in SVG format.

Return back to the “Template — App Icons” layer and you will see every app icon automatically populated with the new icon. 🎉

![BF8B4180-CB13-4E3D-A4B8-4DEB86D11B3C](https://user-images.githubusercontent.com/13254616/169708269-89a9daa6-ad29-4f0d-a2bf-0ba460091c1b.png)

## Exporting from Sketch

The Sketch template is automatically configured to export each icon as its own file, which you can then easily drag and drop into Xcode.

> In the left panel, remember to hide the “App Icon Mask” by clicking on the eye toggle.

Unfortunately, if you export everything at once, some of the icon files will overwrite each other because they have the same name. Exporting in Sketch doesn’t include the folders each icon is situated in, so you’ll have to export each set individually.

To export each set, select all the icon layers in a folder, go to **File**, and click on **Export Current Selection**. Save these files in a folder, e.g. “@2x”.

![0D536EF7-BC15-4D90-9309-4DF2B101040C](https://user-images.githubusercontent.com/13254616/169708317-cc48c252-a222-4f8d-8705-c0ff73a49593.png)

## Importing into Xcode

Your goal now is to match each icon to its respective slot in Xcode. This part might be a little confusing, as it was for me.

In Xcode, find the “Assets.xcassets” file and click on “AppIcon” to view its image set.

![D1B4729F-DF00-403D-A39A-DA67D1B6D0FD](https://user-images.githubusercontent.com/13254616/169708341-b57cc32c-a72d-4bc2-8190-355e17bb84b3.png)

I like to use the guidelines provided in the Sketch template to help me do the math.

![83E1B5D1-23FC-4BE8-9295-E3B0A875C585](https://user-images.githubusercontent.com/13254616/169708371-f4b50512-ca6f-4835-a66f-1cd5c8862bb3.png)

For example, a **20pt x 20pt @2x** icon (the file in the “@2x folder” is called “Icon-App-20x20.png”) means it is **40px x 40px** (what Xcode wants).

Drag each icon file you downloaded from Sketch to its respective slot in Xcode.

![812CC6B0-D12E-404C-830E-095168ADAACB](https://user-images.githubusercontent.com/13254616/169708416-e9b6da68-85aa-4db0-8564-a06a621ae9cf.png)

If you do it incorrectly, Xcode will show you a warning saying that it’s the wrong size or resolution.

![545E3604-4E0F-4C61-95B3-17851A3A4263](https://user-images.githubusercontent.com/13254616/169708429-cf5ea3d1-06ad-4d05-9d0a-b0e2cef1c5ce.png)

Just delete it or drag in the correct icon.
