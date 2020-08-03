## Categorical CSS - Highly Opinionated CSS File Structuring

**If you're very clear where it goes, then you're also very clear where to go to find it again.**

Categorical CSS is designed to provide a categorical highly defined approach to managing your CSS definitions in a clear file structure.

Categorical: **Being without exception or qualification; absolute OR Of or relating to a category or categories.**

The term categorical speaks of the ambition of the project towards provding a very high level of clarity around CSS file naming conventions, 
rather than the ability of the project to ever achieve a spec that is 'without exception'.


CSS is a mess and despite many great attempts to slice and dice it, it remains fairly disorganised.

Currently this README defines the spec.

## Background

The rise of functional and modular CSS have together highlighted the desire to keep CSS more organised.

"Quote on how hard CSS can be to manage"

Modular CSS provided an easy conceptual win by isolating CSS with the component it was design for.
This makes CSS cleaner, but still does not address the more reusable parts of CSS.
Modular CSS can be used in isolation, it also can easily be used along side functional CSS and a functional CSS library.

Functional CSS provided a massive conceptual leap for maintaining CSS.
Naming things is hard, and generating endless names that provide a weakform grouping and abstraction over a set of CSS definitions, proved to be a flawed logic.
Functional CSS addressed this by taking an approach of having each function essentially define a single CSS definition.


## Rationale

There are many ways to group and sort CSS files. 
One thing that defines the current landscape (in 2020) is that multiple filenames are common and accepted and variation of naming conventions is more prevalant than the use
of well established naming conventions.

### Sort like with like

Primarily the filenames reflect the nature of the css element.

* h1,p,strong will re-define inbuilt html elements and go in elements.css
* @font-face definitions can easily and logically be grouped together in fontfaces.css
* @keyframe definitions similarly and unambigiously be grouped together in keyframes.css
* .classes-like-me are considered as defining functions and go in function.css

We split out functions.css with additional files to handle some very common scenarios.

* .image-coffee-chat lets you define positining and scaling around images in images.css
* button .active is about defining the 'original web component' being the inbuilt button and anchor tags, in button.css

# CSS File Naming Convention

| Filename Convention | Inclusive of                   | Description                              | Example                  |
|---------------------|--------------------------------|------------------------------------------|--------------------------|
| elements.css        | Core HTML elements (No ./#/--) | Native HTML Elements (No Classes or IDs) | body, h1, p, a           |
| fontfaces.css       | @fontface                      | Fontface declarations only               | @fontface                |
| keyframes.css       | @keyframe                      | Keyframe declarations only               | @keyframe                |
| variables.css       | --variables                    | Custom Variable definitions only         | --display-mode: dark     |
| functions.css       | .classes #ids                  | Custom functional class/id definitions   | .-z-10                   |
| images.css          | .classes #ids                  | CSS to define image positions            | .image-coffee-chat       |
| buttons.css         | button, a, input .classes #ids | CSS to define button components          | button .active, a .hover |


















