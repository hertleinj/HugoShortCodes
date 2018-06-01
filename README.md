# Hugo Google Maps Shortcodes

On creating my personal Blog with Hugo i found the need to embed maps within my posts.

A short Google search revealed a little help but not the full options that the google API provides. Because of this i began creating my own Shortcodes for this.

## Installation

I suggest to store the shortcodes in a **shortcodes** Folder within the **layouts** Folder, like you can see below.

![Store shortcode Files in layouts/shortcodes](./shortcodes.png)

In addition to this you have to generate yourself a Google API Key. This is possibel at [Google Console](https://console.cloud.google.com/apis/). The generated Key then must be inserted in your sites configuration file.

```toml
[params]
   	googleMapsAPIKey = "XXX"
```

After that they are ready for use in your Markdown Posts. 

## Use

Just add one of the follwoing lines:

```
{{< google-maps-location height="300" location="Nuernberg Germany" >}}

{{< google-maps-direction origin="Nuernberg Bavaria" destination="Frankfurt, Hessen">}}
```

To see the full range of Options for embeded Maps, you can visits [Google's Guide](https://developers.google.com/maps/documentation/embed/guide). All four types are avaliable as shortcodes. The **four** examples above only contain the required Arguments. For all optionals Arguments please refer to the previously mentioned Google Site.

Futhermore you can set the following three parameters for the iframe HTML element:

- scrolling [default: no]
- width [default: 100%]
- height [default: 300px]

## Notice

Please feel free to add Issues or create Pull Requests in the repository. I am new to Hugo and Frontend-Dev is not daily job.