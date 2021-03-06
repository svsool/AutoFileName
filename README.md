AutoFileName: Autocomplete Filenames in Sublime Text
=====================================================
Do you ever find yourself sifting through folders in the sidebar trying to remember what you named that file? Can't remember if it was a jpg or a png? Maybe you just wish you could type filenames faster. *No more.*

Whether your making a `img` tag in html, setting a background image in css, or linking a `.js` file to your html (or whatever else people use filename paths for these days...), you can now autocomplete the filename. Plus, it uses the built-in autocomplete, so no need to learn another *pesky* shortcut.

Usage
=====
If you are looking to autocomplete an image path in an HTML `<img>` tag:
   ```<img src="../|" />```

Pressing control+space, will activate AutoFileName.  I list of available files where be ready to select.

*Looking for an even more automatic and seemless completion?*  Add the following to your User Settings file:
```javascript
    "auto_complete_triggers":
    [
      {
         "characters": "<",
         "selector": "text.html"
      },
      {
         "characters": "/",
         "selector": "string.quoted.double.html,string.quoted.single.html, source.css"
      }
    ]
```

With this, there's no need to worry about pressing control+space, autocompletion with appear upon pressing /.

Now it's more flexible, you can add resources folder in json config of your project. By default json config is package.json, but you are free to choose, just add parameter in your Preferences.sublime-settings

```javascript
    # config name
    { "afn_resources_file": "package.json" }

    # resoureces path in config
    { "afn_resources_param": "_afn_resources" }
```

example of my config
```javascript
    {
        "name": "test",
        "description": "test",
        "version": "0.0.1",
        "private": true,
        "dependencies": {
            "express": "3.x"
        },
        "_afn_resources" : "/path-to-assets/img/"
    }
```