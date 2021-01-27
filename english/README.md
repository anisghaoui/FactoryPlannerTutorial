# FactoryPlannerTutorial
The tutorial for the Factorio Factory Planner Tutorial

The [mod itself](https://github.com/ClaudeMetz/FactoryPlanner/).

# Summary
1. Prelude
2. Introduction
3. The interface
4. Basic example
	1. Timescales
	2. Interpreting the production line
5. Sub-factory levels
6. A bit of complexity

# The tutorial
## Prelude:
This tutorial is written for Factorio version 1.1.19 with the mod Factory Planner version 1.1.17.

## Introduction:
This mod aims to help you calculate what you need to build in order to achieve a certain production level. It basically answer the question: "How many machines will I need to have X items of Y per minute?". It does the computing on your behalf.

Before going further, I feel compelled to inform you that there are other tools to do the same task with each their own variant and flavour. To name a few: helmod mod, kickmcdonalds' website, factorio cheatsheet.

##The interface:
In-game, to open the mod's interface you can:
-Click on the FP button in the top left corner
-Press the (default) shortcut "*ctrl+r*" 
-Click on the FP button in your toolbar

[in game](figure/in_game.png)

You are faced with the main interface as shown in the figure below.

[in game interface](figure/main_interface.png)

*note*: if the interface is to big, press "*esc*" twice, then "*settings*", "*mod settings*", "*per player*" : reduce the width and height then confirm. Ignore everything else for now.

In the main interface, you notice 4 distinctive parts :
* In red: the game subfactories info
	.This area lists everything you have worked on and allows you to exchange it with other people via string exchanges.
* In blue: subfactory info
	.This area contains detailed informations on the current selected subfactory (we will need later)
* In yellow: the outputs, by-product and inputs
	.This area will show you the amounts you will be outputing and inputing in the factory. The by-products are "*unwanted*" results from certain recipes. This is by far the most important area. 
* In green: the production lines
	.This area is the reason why the mod exists. It will display the numbers! and allow you select what your subfactory will do.

Finally, you do notice that there are "*Tutorial*" and "*Preferences*" tabs. As there name indicates, they respectively provide hints and tips, ways to configure your subfactories in terms of machines, belts, etc...

Now that you are familiar with this view, let's use it!

## Basic example:
So, let's say that we need to produce some "*iron gear wheels*". First thing we will press on the only green button that is on the interface. You will be asked to input at least a name or an icon and confirm. You will notice that a new element in the red area appeared. It is a new sub-factory! Click on it and you start editing what that sub-factory does.

[gears](figure_interface/gears.png)

We want to produce "*iron gear wheels*". So it is a product. Let's click on the "*plus*" below the products and search for the desired item as in figure (gears_selected). and let's produce "*15*" of them.

[selected gears recipe](figure_interface/gears_selected.png)

You might be wondering: "*15 what?*". It is *15 items/whatever timescale* is selected in the blue area. In this case, you can see it is 15 *items/min*. Confirm.

Click on the iron gear wheel product to set a recipe for it. It will automatically add a new row in the green area and the required ingredients (in this case "*iron*").

[gears recipe](figure_interface/gears_recipe.png)

Something is wrong... It is showing 0.0 "*iron plates*" and 0.0 "*iron green wheel*". This where you may want to set the disàplayed amount/timescale to your desire. As shown in the figure below, you can select one display modes and timescale:

[modified gears](figure_interface/gears_modified.png)

### Timescales: 
They allow you to scale your production by time. If you want to produce 15 "*iron gear wheels*" per minute and would want how does that scale to an hour or second in game, you just press the buttons (1). FP will automatically recompute the new values and update everything seemelessly.

*Note*: Changing timescale doesn't change your production rate. You will produce the same amount.

We will select timescale as 1 minute.

The display options:
-items/m : the basic display of items flow
-(icon) belts : it shows how many belts will be needed.
-Wagon/m : fluid or cargo weagon needed to maintain such flow
-items/s/machine : the consumption of a single machien in a second. usefull for knowing the inserters count needed.

We will select items/min.

### interpreting the production line:
FP will show you in a row: 
* Resulting item 
* Fullfilment percentage: the ratio resulting items this recipe will produce. For example, you can put 50 % on a row and duplicate it to have the full production. This will be useful to avoid excess amounts of by products.
* Machine: specify the machine tier you will be using. You can click and choose any one you like/need. 
* Module/Beacons: if the machine you are using accepts modules, you select which and how many you will be using in the machine. Click on the "+" next to machine to do so. For the beacons, click on the "+" under beacons. Select the desired beacon. Precise many beacons will affect a machine. select a module to place in the beacons and their count.
* Power: the power consumption of the row.
* Products: what and how much the recipe produces.
* Byproducts: the excesses or side products the recipe produces. You want to deal with these or else your subfactory will get cloged.
* Ingredients: the inputs of the row
* Fuel (optional): if the recipe requires a fuel, it will be displayed as an blue shaded input.

*Hint*: you can alt-click the machine and beacon to put them in your cursor!


You can click on ingredients to set them as a new recipe. This will create a new row and do the same thing to the "*iron plates*". FP will decompose the selected recipe until you are statisfied.

We want to know how many mines we need. Let's decompose all the recipe until we reach the ores! The result should be as displayed in the figure below.

[unrolled recipe](figure_interface/recipe_unroll.png)


First thing, **congratulations**! you have done it! you made it! your very first recipe on Factory Planner. ps: it is automatically saved


## Sub-factory levels:
FP offers a very powerful tool: the sub-levels. See how we selected a way to make iron gear wheels? let's create a red science production of 15 items/second with blue machine and yellow belts.

The result should be as below :
[red science](basic_recipe/red_science.png)

Warning: "*OH NO, I got this huge error! what do I do?*"
Answer: "*simply press cancel, then ctrl click the last row's recipe*"
[red science](basic_recipe/dependence.png)

Now that you have red science, next step green, gray, blue, purple then yellow. Ohh that a lot! it will result in a horror that I can't even printscreen. Here is the exchange string instead:

```
eNrtXduO2zYQ/Rc9W4t1gRSFXwMUKNAFgvaxWBgUNbLZ8qIOKbuu4X/PUJe9xBtYbhqb8g7ysqYo8pCHc+FwxOwz48rlBtArZ7NFNr+jfx+yWQb/1A7Dkp56CNlinxXCQ1/hJ3peCRkc7motrAV8+WalVUG/7+9+vJtnh1nmm6KrrMBniz/2mRUmtkRVlYyd7rOwq2OJCmCotH8umuCMCIQr91KBlZDXQv4VmwzKgJdCU7U51Xchthwb/ISubGSL1xV/ggxdjzW64GLhiaYJrDK1VpWCMlsEbGD2Cht1jfB3oxDKpTCusW1PJVTKUkmxi013xbPhj8X8QwTs6qWGDeihVamFj5gHwIfZMUrtVsoHJVPGaJRWQeAuZYxyDUbRakkZY909S3xFNiHSnQ7Zj7NezJfDo186FTL8/Oi0hnZas77BSjuHEcCv1P2XemJ4rX0WYUtVt5X+80RIEWBFejIuQxRVUHYVkTzTveynqiuBF9h/63qn2qQ91QaGJksXgVdCe/pRA0qwQayiKry/n2VGyHU/siOt5z2YQhOEvK+Vz88BXTnqa6mVUeGp/wdCrV/P4/5wxEpf62u8mPbxUnbc3z9Xe+gHc4iLcTQ558gS83N5fsbbDGbn8uyMt5bMzuXZGe8TMjuXZ+ecfUXi/Pxwk7rN1TQtOW1aA5wanzegr0qKD/RmXjVohTwL7VtsVE10o9+aEaFPMt1bhNj2MNqfY3uHNFlWSPK3AoH5dg2gWfpS4cXUjhY15r0YOjy5rAvho61zWpVXowfijCDBMMpGjkpUWp8JfDIURdFh9Xjb6nEQw5ZsFsKU9aTQUyCnICEkff4/U/OuZNJ6wADIO7lECAkorI8nYHlBloNpSYSWzgw4S7pDKpSNYmoS21tLUWhgUtI5CpHgfRxnY8cLS75VYZ1XurmiU/Etu+Iv8E+FrUrvInh0hQt5hbGQBSmVuPs2L8H69tCXRiRDg8xOKuygUJrJSMpHIw9tZGyGiblwXsQmKjEzdM3cJMGNoknpjH9jS0+DXYl/u5eYoBQIWiFYUTIfqfDRhf+3QrPhT4aSRpPJHxWaJRd6dzU+njKcYvJ6OAvvZBJRyo2wEkqOkqXmHNtVHNuYYMwzh1Mk50300zEuAJrPwW/7zK0QIQAhZ3uVUMzgDP3Iwerr7lipYkxELgS7fElljbQGgXN6Ekysi/LCyfppRRAKHMEJO3lTdfIqhSDQcDw1vYB3zWSkFbkjuyokmVX25hLIN2iiYTp3dMzGd/attzQQzF1V+bVDyOvG1KcG/LrytUj6Nsj8+Qp7dPx1H/sQnJrNqdlMCn+LztaKo7L8uTNL4BQkkLOSOPmFk194g3UD51WclHTz1oqPRfimFPbf+UYpvsyGL7OZfMyDKX8vlD9teJwiF/Xp0omTB42va1/tcJRgYHsf/el08GPI19TExxfg91S93WJ/m/78xaJqr8N/scp+H/63jl12eDx8BtTKkro=
```

On the top left corner, click on "import a factory". Import then confirm. 

You can see the many flaws I created while doing such a task. The smarter way to do this would be to use the sub-levels:
* Create 6 sciences recipes
* Click on each recipe to enter the sub-level
* Build your recipe as you want it. If it is too complicated (~~looking at you purple and yellow~~), you can create a new sub-level.

## A bit of complexity:
You may have noticed that it gets really clumsy when having recipes that consumes the same ingredients but FP is too stupid to factor that in and, instead, displays 2 differents rows... you may also wonder what is this button called "*matrix solver*".

Let's try to produce a lot of "*lubricant*". Oil recipes have usually feedback loops, meaning a fraction of the output in sent back to the input. This is where the algebric solver (the one we have been using until now) is limited. Create a new lubricant recipe. you should obtain the following :

[lubricant](matrix_solver/lubricant.png)

sigh... there are 2 by products. I wish I could turn them into plastic and rocket fuel. Trying to click on the said byproducts will have FP display a red message. The default solver is indeed unable to solve this. **Dare** and toggle on the "*matrix solver*".

You can now select recipes that will consume the byproducts! Notice how you can't control statisfaction percetage anymore. It is automatically deduced from the matrix

```
eNrtXN+P2zYM/l/8HB8uBToMeR0wYMAKDNvjUBiyTCfcZMuj5KRZkP99pH/0Lk26xOsQK61wD4klhfrIT6Qo2r5DUtki2wI5tHWySpZP/Pc2WSTwobHkM+514JPVIcmVg2HA99xfKu0t7Ruj6hro9S9LgzlfPz9997RMjovEtXk/GMElq98PSa0qkcRDUcukh8TvG2lBDxW3Dv2uURpSpxFq/uSLP0WaxwqcVoZHLHmo9SJUZP1Ctmh1B9Xmf4D2/WQNWW+lcZCqWm8r5VnbU9GME6vGYIlQJCtPLSxOYPHUBH+1SFBkqrJt3c1UQIk1t+R7Ed03L8Yvq+VbAWybzMAWzChVG+UE8wj4uDhHaewanUcdMsYKDXpF+5Ax6g1UyKslZIxN3xf4imy90B0O2e8Xg5tnY9dPffQYL3+wxkBnVoHBLk/4ISsJIBNoJ5FoA2q7Ty2af1OoNC0W3bwCrjTWkijzM6vyacwZIXR9fQCcMJxAY9MN+pLYpZWHNQdocQJSpcd6LXZ4WWzZoFffAq8s92sPgEdz2MYtjCILK9hLZRxfNEAaaq/WEoifn8XCejMod4bbOahywxDSYVT6Zgro0vJcmcEK/cf53zFqc2rKw/FsTQyjPrsquu5M9yvv+WXYu0GZo7jCzfxo27BZUt4TPVzTz1VgZiXFef5lWrZUKz0J7SU2ylZc9ZJFlLnK9BCjRfao7Y8i7xgmy0jsf2tQlO42ACZ6X0i8RN/7un2vaiwbj9KObEtXjcenFsmirZG9eya2QexBDKPCWrywIDRmIvCHccKRoFtWXyRnNnK6RCX6z10oOj+qDExdljice968isjd6eES1//b0eL2gkNMbe7vuJ5U7aQel+acC0RaQomntQPyQJGQQAjpdwpbcxzTSLrF6CuB1Ua0yg1EUr7xbOP2WwdxVdzfVRtko4iWxAILx8qu1d/DCogEBUDQmqBWReQjFD76ct5OmVgMDocSABOrwV93NbhEAkVV3KDCDIg54fWsLnrfw9+L6SwYC8nxaDftiasYmGcIzK3hSHdTJHKev8/Fx8dVJM+X+kl4H4UKVWwV+0cRK5WhFZHrtejW1tc5eeHwEcm5iP5xilRNzPeDIYMHys3jXMW9JajUfMeKUGrL0m0scS7WVs01hU8Hz0XSl0F+uBzAIi9HshqcE9e/pu/p6Nk4YhjUPcvPqCZDjgepKzF1wmshcc+7v++SwljuD+vBD85AbqzjRWLulRkOxt3Ku2PVOHXkJpgXJiRvj5vKt55s3Px2Z1wUs8TQIW++qSg1qpju0G/S4bXVB6ToE/yPwlZp9v2zU7n1aUnSGB0pDGqM3aUF1K6LdKyR9i1FdsK6N8U5vNLs8bGMOD8jufL+htpO5OKeJ9wJt6diJjDvdtPKE1BTF2R0oBmOVv9N0PJM0EvDb+N/vWIjvT/+Ay/dBF8=
```


### How does it work?
If you want to produce X *iron gears*, you need 2 X *iron plates*


# Contribution