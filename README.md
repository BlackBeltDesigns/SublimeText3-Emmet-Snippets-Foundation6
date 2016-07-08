# SublimeText3-Emmet-Snippets-Foundation6
Foundation 6 snippets with options for Emmet in SublimeText 3

<a target='_blank' href='https://pledgie.com/campaigns/32195'><img alt='Click here to lend your support to: Sublime Text 3 Emmet Dynamic Snippets for Foundation 6 and make a donation at pledgie.com !' src='https://pledgie.com/campaigns/32195.png?skin_name=chrome' border='0' ></a>

# Instructions
* You will obviously need the following prior to doing anything with this repo...
  * [Sublime Text 3](https://www.sublimetext.com/3)
  * [Emmet](http://emmet.io/)
  * [Foundation for Sites 6](http://foundation.zurb.com/sites/getting-started.html)
  
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

##How to use them

These all output dynamic emmet snippets allowing for the referenced Foundation 6 elements. In other words, when you tab complete, you aren't actually "completing" the snippet. You are loading the emmet snippet and filling in the variables available for that Foundation 6 element.

Take this simple example:

An **Accordion** in the Foundation 6 example is like this:

```
<ul class="accordion" data-accordion role="tablist">
  <li class="accordion-item is-active">
    <!-- The tab title needs role="tab", an href, a unique ID, and aria-controls. -->
    <a href="#panel1d" role="tab" class="accordion-title" id="panel1d-heading" aria-controls="panel1d">Accordion 1</a>
    <!-- The content pane needs an ID that matches the above href, role="tabpanel", data-tab-content, and aria-labelledby. -->
    <div id="panel1d" class="accordion-content" role="tabpanel" data-tab-content aria-labelledby="panel1d-heading">
      Panel 1. Lorem ipsum dolor
    </div>
  </li>
  <li class="accordion-item">
    <!-- The tab title needs role="tab", an href, a unique ID, and aria-controls. -->
    <a href="#panel1d" role="tab" class="accordion-title" id="panel1d-heading" aria-controls="panel1d">Accordion 1</a>
    <!-- The content pane needs an ID that matches the above href, role="tabpanel", data-tab-content, and aria-labelledby. -->
    <div id="panel1d" class="accordion-content" role="tabpanel" data-tab-content aria-labelledby="panel1d-heading">
      Panel 2. Lorem ipsum dolor
    </div>
  </li>
  <li class="accordion-item">
    <!-- The tab title needs role="tab", an href, a unique ID, and aria-controls. -->
    <a href="#panel1d" role="tab" class="accordion-title" id="panel1d-heading" aria-controls="panel1d">Accordion 1</a>
    <!-- The content pane needs an ID that matches the above href, role="tabpanel", data-tab-content, and aria-labelledby. -->
    <div id="panel1d" class="accordion-content" role="tabpanel" data-tab-content aria-labelledby="panel1d-heading">
      Panel 3. Lorem ipsum dolor
    </div>
  </li>
</ul>
```

In order to do this in ST3 using Emmet, you would do something like this:

```
ul.accordion[data-accordion role="tablist"]>li.accordion-item.is-active>a.accordion-title#panel1d-heading[href="#panel1d" role="tab" aria-controls="panel1d"]{Accordion 1}+#panel1d.accordion-content[role="tabpanel" data-tab-content. aria-labelledby="panel1d-heading"]{Panel 1. Lorem ipsum dolor}
```

Then hit **TAB** which would output:

```
<ul class="accordion" data-accordion="" role="tablist">
	<li class="accordion-item is-active">
		<a href="#panel1d" class="accordion-title" id="panel1d-heading" role="tab" aria-controls="panel1d">Accordion 1</a>
		<div id="panel1d" class="accordion-content" role="tabpanel" data-tab-content aria-labelledby="panel1d-heading">Panel 1. Lorem ipsum dolor</div>
	</li>
</ul>
```

You could then copy the inner **li** and paste it the amount of times you wanted and edit the **ID's** accordingly or add a `*x` where 'x' is the multiple of times you wanted an li in the original snippet.

##INSTEAD, with this repo...
...you simply type:

`accordion` and  **TAB** which gives you the following:

```
ul.accordion[data-accordion.]>(li.accordion-item[data-accordion-item.]>a.accordion-title{Accordion}1+.accordion-content[data-tab-content.]{lorem25})*how_many
```

When this is output, it stops and highlites the `25` in `{lorem25}`.

Select how much lorem text you would like in your output containers and hit **TAB** again. This time it stops on `how_many`. Simply enter the number of `li` elements you want. (Or the number of `accordion` containers you want).

Now you can either tab to complete the code or go back to the end of the `lorem` spot and output the lorem code before finalizing. Then end of line and **TAB** to output the markup.

If I enter `30` for the `lorem` and `4` for the `how_many`, I will end up with the following:

```
<ul class="accordion" data-accordion>
	<li class="accordion-item" data-accordion-item>
		<a href="" class="accordion-title">Accordion</a>
		<div class="accordion-content" data-tab-content>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reiciendis quos cupiditate perspiciatis animi voluptates nostrum aut, aperiam ex nulla esse, molestiae adipisci iure harum hic. Architecto autem culpa, similique delectus!</div>
	</li>
	<li class="accordion-item" data-accordion-item>
		<a href="" class="accordion-title">Accordion</a>
		<div class="accordion-content" data-tab-content>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reiciendis quos cupiditate perspiciatis animi voluptates nostrum aut, aperiam ex nulla esse, molestiae adipisci iure harum hic. Architecto autem culpa, similique delectus!</div>
	</li>
	<li class="accordion-item" data-accordion-item>
		<a href="" class="accordion-title">Accordion</a>
		<div class="accordion-content" data-tab-content>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reiciendis quos cupiditate perspiciatis animi voluptates nostrum aut, aperiam ex nulla esse, molestiae adipisci iure harum hic. Architecto autem culpa, similique delectus!</div>
	</li>
	<li class="accordion-item" data-accordion-item>
		<a href="" class="accordion-title">Accordion</a>
		<div class="accordion-content" data-tab-content>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reiciendis quos cupiditate perspiciatis animi voluptates nostrum aut, aperiam ex nulla esse, molestiae adipisci iure harum hic. Architecto autem culpa, similique delectus!</div>
	</li>
</ul>
```

You can now knock out a fully responsive sample site with demo content in it in no time.

---

##Here are the ones available:
_(for ease of use, I named them what they are so they can be easily located in the Foundation 6 docs)_

* "menu"
* "menu:bar"
* "menu:drop"
* "menu:drop:vert"
* "menu:drill"
* "menu:accordian"
* "button:tiny"
* "button:small"
* "button:large"
* "button:expanded"
* "button:expanded:small"
* "button:group"
* "button:group:small"
* "button:group:expanded"
* "button:group:stacked"
* "button:group:stacked:small"
* "button:group:stacked:medium"
* "slider"
* "slider:vert"
* "switch"
* "switch:tiny"
* "switch:small"
* "switch:large"
* "switch:text"
* "switch:radio"
* "pagination"
* "breadcrumbs"
* "accordion"
* "dropdown"
* "dropdown:hover"
* "off-canvas"
* "modal"
* "modal:tiny"
* "modal:small"
* "modal:large"
* "modal:full"
* "page"
* "tables"
* "tables:hover"
* "tables:stack"
* "tables:scroll"
* "tabs"
* "tabs:vert"
* "video"
* "video:youtube"
* "video:vimeo"
* "slider:image"
* "slider:text"
* "tooltip"
* "equalize"
