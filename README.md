# SublimeText3-Emmet-Snippets-Foundation6
Foundation 6 snippets with options for Emmet in SublimeText 3

# Instructions
* Download this repo and unzip.
* Create a folder in SublimeText 3 > Packages > User
* Use the Menu to open the `Emmet.sublime-settings` file 
  * `Preferences > Package Settings > Emmet > Settings-User`
* This will open up the settings file in your `User` folder.
  * Take note at the path where this file is.
* Now create a new folder in the `User` folder
  * Name it whatever you like.
    * I used `Extensions`
* For clarity, I also created a folder inside this named `Emmet`.
* Now place the `snippets.json` file from the repo download inside this folder.

__You should now have something like the following:__

*%APPDATA%\Roaming\Sublime Text 3\Packages\User\Extensions\Emmet\snippets.json*

* Next you will need to go back to the `Emmet.sublime-settings` file you opened earlier.
* Change your `"extensions_path"` variable on line 7 to the location we made.
  * It should look something like this when comleted:
    * `"extensions_path": "~/AppData/Roaming/Sublime Text 3/Packages/User/Extensions/Emmet",`
* Restart Sublime Text 3 and enjoy the speedy clips!
 
---

_Please reference the [Foundation for Sites Docs](http://foundation.zurb.com/sites/docs/kitchen-sink.html) to see all posibilities. I didn't create dynamic snippets for all elements, but did create the ones most used._

##Here are the ones available:
_(for ease of use, I named them what they are)_

"menu"
"menu:bar"
"menu:drop"
"menu:drop:vert"
"menu:drill"
"menu:accordian"
"button:tiny"
"button:small"
"button:large"
"button:expanded"
"button:expanded:small"
"button:group"
"button:group:small"
"button:group:expanded"
"button:group:stacked"
"button:group:stacked:small"
"button:group:stacked:medium"
"slider"
"slider:vert"
"switch"
"switch:tiny"
"switch:small"
"switch:large"
"switch:text"
"switch:radio"
"pagination"
"breadcrumbs"
"accordion"
"dropdown"
"dropdown:hover"
"off-canvas"
"modal"
"modal:tiny"
"modal:small"
"modal:large"
"modal:full"
"tables"
"tables:hover"
"tables:stack"
"tables:scroll"
"tabs"
"tabs:vert"
"video"
"video:youtube"
"video:vimeo"
"slider:image"
"slider:text"
"tooltip"
"equalize"
