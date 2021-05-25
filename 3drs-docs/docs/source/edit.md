# Edit representation

Once the structure or structures are uploaded, users will be redirected to the **Edit representation page**. This page loads the structure(s) and shows a notification warning that the project will expire unless it’s shared. That means that users have **until the date shown** in the notification for editing and sharing a project. In case of not sharing it after this period of time, all the files and data related to the project will be **removed** from our database.

In the 1.0.0. version, the expiration time is **20 days**.

Following the philosophy of the project, this **Edit representation page** is open, but protected so that only user(s) with this URL address can access it.

This **Edit representation page** is the core of the application and we can split it into five parts:

![](_static/edit/edit01.png)

* **[Stage](#stage)**
* **[Tools](#tools)**
* **[Representations](#representations)**
* **[Selections](#selections)**
* **[Share](#share)**

## Stage

![](_static/edit/edit02.png)

The **stage** covers the entire screen and the rest of the parts are on top of it. In the stage the **structure is loaded** and users can interact with it in several ways. At this point it’s important to remember that **this application has no Save button**. Each change performed over the stage or panel will be **automatically saved** to the database, so anytime a user can close the browser and then come back to keep working on the edition at the same point it was.

### Zoom / Drag

Actions of **zoom in** and **zoom out** can be done with the **scroll mouse or the trackpad** of a notebook:

* Clicking **out of the structure** (that means in the “empty” part of the stage) with the **left button** and **dragging will rotate the view**.

* Clicking **out of the structure** (that means in the “empty” part of the stage) with the **right button** and **dragging will translate the view**.

* Double clicking **out of the structure** (that means in the “empty” part of the stage) with the **left button** will center the view.

### Mouse actions

#### Mouse over actions

Passing the mouse over the molecules of the structure will **highlight** them and show **their information** in the **legend** on the bottom right of the stage.

#### Mouse click actions

* Clicking with the mouse **left button** on a molecule will **select it for the current representation**. Note that the **representations are explained in the Representations section**. Only a **new representation** accepts **new molecules**. In the **default representation** no molecules can be **selected** and this feature is disabled.
* Clicking with the mouse **left button** on a molecule **while pressing the Ctrl key** will make a zoom in at a molecule.
* Clicking **consecutively on two atoms** with the mouse **right button** will draw and calculate the distance in **ångströms** between these two atoms. In the **default representation** no distances can be **created** and this feature is disabled.
* Clicking **consecutively on three atoms** with the mouse **right button while pressing the Ctrl key** will draw and calculate the angle in **degrees** between these three atoms. In the **default representation** no angles can be **created** and this feature is disabled.

### Legend

![](_static/edit/edit03.png)

As explained in the previous section, passing the mouse over the molecules of the structure will **highlight** them and show **their information** in the **legend** on the bottom right of the stage. This legend shows information about the molecule in the next format:

**Structure file name** | Model **number** | Chain **ID** | **Residue name (Residue long name) Residue number** Atom name (or Bond)

## Tools

The tools menu is at the top left of the **stage** and allows users to make some actions over it:

![](_static/edit/edit04.png)

* **[Reload](#reload)**
* **[Center](#center)**
* **[Background](#background)**
* **[Full Screen](#full-screen)**
* **[Superposition](#superposition)**
* **[Measurements](#measurements)**
* **[Navigation mode](#navigation-mode)**
* **[Help](#help)**
* **[Project settings](#project-settings)**

### Reload

![](_static/edit/edit05.png)

Clicking this button **restores the view to the initial position** on the **stage**.

### Center

![](_static/edit/edit06.png)

Clicking this button centers the structure(s) position on the stage.

### Background

![](_static/edit/edit07.png)

Clicking this button opens a color picker that allows users to change the background color of the stage.

### Full screen
IMAGE OF BUTTON

Clicking this button opens the fullscreen mode. For exiting full screen mode, just click the button again or press the Esc key.

### Superposition
IMAGE OF BUTTON

TODO!!!!!!!!!!!!!!!!!!.

### Measurements
IMAGE OF BUTTON

Clicking this button opens a modal dialog to edit the distances and angles created by users in the stage. For remembering how to draw them, please go back to the Mouse click actions section.

### Navigation mode
IMAGE OF BUTTON

TODO!!!!!!!!!!!!!!!!!!.

### Help
Link  to this same Read the Docs.

### Project settings
IMAGE OF BUTTON


Clicking this button opens a modal dialog to edit the project settings.

IMAGE OF SETTINGS

Project title: title of the project. If this field is empty, neither title nor caption will be shown in the project once shared
Representation caption: representative information of the project such as description, author(s), links and so on.
Fork project when shared: if enabled, the project will be able to be forked once shared. That means that anyone can make an editable copy of the project.
Overlay messages: there are notification messages for almost each action in the application. With this button they can be enabled / disabled. Note that although this option is enabled, the expiration notification will still appear as well as some error messages.
Creation date: date of creation of the project.
Expiration date: date of expiration of the project. This date will disappear once the project is shared for the first time, since then the project will be persistent.
Representations
The Representations panel is at the bottom left of the stage and is used for changing the properties of the representation.

Initially, there is a Default representation that only allows to change the opacity and hide or show it:

IMAGE OF DEFAULT REPRESENTATION WITH LABELS

Once users create a new representation, there are all the properties available:

IMAGE OF COMMON REPRESENTATION WITH LABELS
Representation actions
Below there is a description of all the actions that can be performed in this panel.
Select representation
IMAGE OF SELECT

In this dropdown menu, users can switch between all the representations of the project.

Edit representations
Below the select dropdown menu there is a tiny menu for making some actions over the representations:

Hide / show: hides or show the current representation selected on the dropdown above.
Hierarchy map: shows a modal dialog with all the molecules selected in each representation. In the default representation this feature is disabled.
IMAGE OF HIERARCHY
Edit representation name: allows to rename the current representation. In the default representation this feature is disabled.
Add / remove label: adds or removes a new label to the current representation. If there is more than one structure, it will show as many labels as there are structures. In the default representation this feature is disabled.
Remove: removes the current representation and all the selections linked to it. This button must be clicked twice in order to ensure that it has not been clicked by mistake. In the default representation this feature is disabled.

Representation properties
There are several properties that can be modified for each representation.
Molecular representation
IMAGE OF MOLECULAR REPR

Each loaded structure can be displayed using a variety of molecular representations:

IN EACH POINT SHOW THE SAME STRUCTURE WITH THE RESPECTIVE REPR.

Backbone: Cylinders connect successive residues of unbroken chains by their main backbone atoms, which are .CA atoms in case of proteins and C4'/C3' atoms for RNA/DNA, respectively. The main backbone atoms are displayed as spheres.
Ball and stick: Atoms are displayed as spheres (balls) and bonds as cylinders (sticks).
Cartoon: The main backbone atoms (see backbone) of successive residues in unbroken chains are connected by a smooth trace. The trace is expanded perpendicular to its tangent with an elliptical cross-section. The major axis points from .CA in the direction of the .O in case of proteins and from the C1'/C3' to C2'/O4' for RNA/DNA, respectively.
If RNA/DNA an additional base representation is added: simplified display of RNA/DNA nucleotides, best used in conjunction with a cartoon representation. Here, a stick is drawn connecting the sugar backbone with a nitrogen in the base (.N1 in case of adenine or guanine, .N3 in case of thymine or cytosine).
Licorice: A variant of the ball+stick representation where balls and sticks have the same radius.
Line: Bonds are displayed by a flat, unshaded line.
Spacefill: Atoms are displayed as a set of space-filling spheres.
Surface: Displays the molecular surface and its variants.
Ribbon: A thin ribbon is displayed along the main backbone trace.

Due to a shortcoming of NGL Viewer, the cartoon and ribbon representations only can show four or more consecutive residues.

The Default representation can’t be edited but represents the structure in a standard way:


Backbone: Cartoon representation.
NA bases (if present): Base representation.
Heteroatoms: Ball and stick representation.
Ions: Ball and stick representation.
Waters: Ball and stick representation.

So take into account that if for example there is an heteroatom with ATOM instead of HETATM in the PDB file, it won’t be shown in this Default representation. 
Radius
IMAGE OF RADIUS

Through this slider, the radius can be modified in the next molecular representations:

Backbone
Ball and stick
Licorice
Spacefill
Color scheme
IMAGE OF COLOR

Each loaded structure can be displayed using a variety of color schemes:

IN EACH POINT SHOW THE SAME STRUCTURE WITH THE RESPECTIVE COLOR

Atom index: color by atom index.
B-factor: color by b-factor.
Chain id: color by chain id.
Chain index: color by chain index.
Element: color by chemical element.
Hydrophobicity: color by hydrophobicity.
Model index: color by model index.
Random: class by random color.
Residue index: color by residue index.
Residue name: color by residue name.
Secondary structure: color by secondary structure.
Uniform: color by uniform color selected from the color picker that appears at right of the dropdown menu when this option is selected.

The colors for the Default representation are as follows:


Backbone: Secondary structure color scheme.
NA bases (if present): Residue name color scheme.
Heteroatoms: Element color scheme.
Ions: Element color scheme.
Waters: Element color scheme.

Opacity

IMAGE OF OPACITY

Through this slider, the opacity of the representation varies. Note that due to an incompatibility of NGL Viewer, opacity in multilayer projects can generate some issues. So creating multiple representations with different degrees of opacity can give non desired outcomes.

Moreover, if the opacity of a representation is less than 30 it won’t be possible to select the residues from the stage. Due to a WebGL problem, the threshold for allowing selections from stage is set to greater than 30.
New representation

In this text box, users should insert the name for creating a new representation. For the sake to clearly see all the items that can be selected in the representation, initially a line representation will be shown. But at the moment that some molecule is selected, the rest of molecules will disappear from the stage. See next section for a more detailed description of this behavior.

IMAGE OF ALL LINE REPR (NEW)

Selections
The Selections panel is at the right side of the stage and is used for applying selections to the current representation selected in the Representations panel.

Note that if the current representation is the Default one, this panel will be disabled. Once users create a new representation, the Representations panel will open automatically though it can be closed clicking the open / close button.

When a new representation is created, all the items in the stage will be selected by default with a Line representation and Secondary structure color scheme. The meaning of this is to easily glimpse all the molecules contained in the representation. Once the first molecule (one of Sequence, Heteroatoms, Ions or Waters) is selected, this one will be the only one selected.

IMAGE OF SELECTION PANEL WITH LABELS
Structures
Select structure

In this dropdown menu, users can switch between the different structures uploaded in the Launch project page.

Opening the dropdown menu and passing the mouse over the structures contained on it will highlight them in the stage.

If there is only a single structure, this dropdown menu will be disabled.
Structures menu
Below the dropdown menu there are a couple of buttons:

Center structure: centers the stage view in the currently selected structure. Note that if there is only a portion of the structure selected, the view will center around this portion.
Custom selection / Manual selection: as explained later on, advanced users can make custom selections using NGL Viewer selection language. When custom selection is clicked, only this panel will be shown in the molecules part of the Structures panel. For coming back to the manual selection just click the same button again
Custom selection
IMAGE OF BLOCK OPEN

For accessing this section, the Custom selection button of the structures menu must be clicked.

In this block, users can add a custom selection written in NGL Viewer selection language. Please visit the Selection language section of the NGL Viewer manual before starting with this section.

Note that custom selection is not compatible with manual selection, so even though the selections made in the manual selection section will not be removed, they won’t be visible in the stage. If users want to restore a previously made manual selection, just removing the custom selection will do the trick.
Models
IMAGE OF BLOCK OPEN

If the selected structure has more than one model, this block will be enabled allowing users to switch between the different models of the structure.

There is a mini menu at the right side of the block header:
Show tips: opens a modal dialog with a short help for this section
Show / hide block: allows to open or collapse the panel.

Note that switching between models will change the succeeding panels (i.e. if the Model 1 has two chains A and B and the Model 2 has three chains A, B and C, the Chains block will change).

If there is only a single model, this block menu will be disabled.

Chains
IMAGE OF BLOCK OPEN

If the selected model of the current structure has more than one chain, this block will be enabled allowing users to switch between the different models of the structure.

There is a mini menu at the right side of the block header:
Show tips: opens a modal dialog with a short help for this section
Show / hide block: allows to open or collapse the panel.

Opening the dropdown menu and passing the mouse over the chains contained on it will highlight them in the stage.

Note that if the structure has no chains, all the molecules will be automatically assigned to the Chain A. If the structure has one or more chains but some of its molecules have no chain, these “orphan” molecules will be assigned to a mock Chain @.

If there is only a single chain, this block menu will be disabled.
Sequence
There are two ways to perform sequence residues selection: directly through the block in the Selection panel or though the Zoom window:
Selection panel block

IMAGE OF BLOCK OPEN

This block shows all the residues of the structure classified by chains.

There is a mini menu at the right side of the block header:
Open / close external window: allows to open or close the Zoom window for this section.
Select / unselect all: allows to select or unselect all the molecules of this block with a single click.
Show tips: opens a modal dialog with a short help for this section.
Show / hide block: allows to open or collapse the panel.

Different actions can be performed with the residues:

Passing the mouse over a residue will highlight it on the stage.
Clicking on a residue will select it in the current selection applying to it the molecular representation, radius, color scheme and opacity selected in the representations panel for the current representation.
Clicking on a selected residue will unselect it from the current selection.
For selecting multiple residues just click the first residue of the custom sequence with the mouse left button while pressing the Shift key. A small cross will be shown next to the mouse pointer. Then, click the last residue of the custom sequence again with the mouse left button while pressing the Shift key.
For unselecting multiple residues is exactly the same process: just click the first residue of the custom sequence with the mouse left button while pressing the Shift key. A small cross will be shown next to the mouse pointer. Then, click the last residue of the custom sequence again with the mouse left button while pressing the Shift key.

Note that multiple selections are only allowed between residues of the same Model and Chain. Trying to select multiple residues from different Model and / or Chain will show an error notification:

IMAGE OF ERROR NOTIFICATION

If there are no residues in the selected structure (i.e. an heteroatom), this block menu will be disabled.
Zoom window
IMAGE OF WINDOW

This window shows the same information of the Sequences block but in a little more detail, adding the ability of selecting α-helices and β-sheets if they are present in the structure.

There is a mini menu at the right side of the window:
Select / unselect all: allows to select or unselect all the molecules of this block with a single click.
Close window: closes the window.

Different actions can be performed with the residues:

Passing the mouse over a residue will highlight it in the stage.
Clicking on a residue will select it in the current selection applying to it the molecular representation, radius, color scheme and opacity selected in the representations panel for the current representation.
Clicking on a selected residue will unselect it from the current selection.
Clicking on a residue with the mouse left button while pressing the Alt key will do a zoom to the residue.
For selecting multiple residues just click the first residue of the custom sequence with the mouse left button while pressing the Shift key. A small cross will be shown next to the mouse pointer. Then, click the last residue of the custom sequence again with the mouse left button while pressing the Shift key.
For unselecting multiple residues is exactly the same process: just click the first residue of the custom sequence with the mouse left button while pressing the Shift key. A small cross will be shown next to the mouse pointer. Then, click the last residue of the custom sequence again with the mouse left button while pressing the Shift key.
Passing the mouse over an α-helix or a β-sheet will highlight it in the stage.
Clicking on a α-helix or a β-sheet will select it in the current selection applying to it the molecular representation, radius, color scheme and opacity selected in the representations panel for the current representation.
Clicking on a  α-helix or a β-sheet will unselect it from the current selection. Note that to unselect a whole α-helix or β-sheet all its residues must be selected.


Note that multiple selections are only allowed between residues of the same Model and Chain. Trying to select multiple residues from different Model and / or Chain will show an error notification:

IMAGE OF ERROR NOTIFICATION
Heteroatoms
IMAGE OF BLOCK OPEN

This block shows all the heteroatoms of the structure.

There is a mini menu at the right side of the block header:
Select / unselect all: allows to select or unselect all the molecules of this block with a single click.
Show tips: opens a modal dialog with a short help for this section.
Show / hide block: allows to open or collapse the panel.

There is a search box on the top of the heteroatoms list that allows users to perform searches on this list.

Different actions can be performed with the heteroatoms:

Passing the mouse over an heteroatom will highlight it in the stage.
Clicking on an heteroatom will select it in the current selection applying to it the molecular representation, radius, color scheme and opacity selected in the representations panel for the current representation.
Clicking on a selected heteroatom will unselect it from the current selection.
Clicking on the Center button of each heteroatom will do a zoom on it.
 
If there are no heteroatoms in the selected structure, this block menu will be disabled.
Ions
IMAGE OF BLOCK OPEN

This block shows all the ions of the structure.

There is a mini menu at the right side of the block header:
Select / unselect all: allows to select or unselect all the molecules of this block with a single click.
Show tips: opens a modal dialog with a short help for this section.
Show / hide block: allows to open or collapse the panel.

There is a search box on the top of the ions list that allows users to perform searches on this list.

Different actions can be performed with the ions:

Passing the mouse over an ion will highlight it in the stage.
Clicking on an ion will select it in the current selection applying to it the molecular representation, radius, color scheme and opacity selected in the representations panel for the current representation.
Clicking on a selected ion will unselect it from the current selection.
Clicking on the Center button of each ion will do a zoom on it.
 
If there are no ions in the selected structure, this block menu will be disabled.
Waters
There are two ways to perform waters selection: directly through the block in the Selection panel or though the Zoom window:
Selection panel block

IMAGE OF BLOCK OPEN

This block shows all the waters of the structure classified by chains.

There is a mini menu at the right side of the block header:
Open / close external window: allows to open or close the Zoom window for this section.
Select / unselect all: allows to select or unselect all the molecules of this block with a single click.
Show tips: opens a modal dialog with a short help for this section.
Show / hide block: allows to open or collapse the panel.

Different actions can be performed with the water molecules:

Passing the mouse over a water molecule will highlight it on the stage.
Clicking on a water molecule will select it in the current selection applying to it the molecular representation, radius, color scheme and opacity selected in the representations panel for the current representation.
Clicking on a selected water molecule will unselect it from the current selection.
Clicking on a water molecule with the mouse left button while pressing the Alt key will do a zoom to the water molecule.
For selecting multiple water molecules just click the first water molecule of the custom sequence with the mouse left button while pressing the Shift key. A small cross will be shown next to the mouse pointer. Then, click the last water molecule of the custom sequence again with the mouse left button while pressing the Shift key.
For unselecting multiple water molecules is exactly the same process: just click the first water molecule of the custom sequence with the mouse left button while pressing the Shift key. A small cross will be shown next to the mouse pointer. Then, click the last water molecule of the custom sequence again with the mouse left button while pressing the Shift key.

Note that multiple selections are only allowed between water molecules of the same Model and Chain. Trying to select multiple water molecules from different Model and / or Chain will show an error notification:

IMAGE OF ERROR NOTIFICATION

If there are no water molecules in the selected structure, this block menu will be disabled.
Zoom window
IMAGE OF WINDOW

This window shows the same information of the Waters block but in a little more detail.

There is a mini menu at the right side of the window:
Select / unselect all: allow to select or unselect all the molecules of this block with a single click.
Close window: closes the window.

The actions that can be performed are the same that in the Waters block:

Passing the mouse over a water molecule will highlight it on the stage.
Clicking on a water molecule will select it in the current selection applying to it the molecular representation, radius, color scheme and opacity selected in the representations panel for the current representation.
Clicking on a selected water molecule will unselect it from the current selection.
For selecting multiple water molecules just click the first water molecule of the custom sequence with the mouse left button while pressing the Shift key. A small cross will be shown next to the mouse pointer. Then, click the last water molecule of the custom sequence again with the mouse left button while pressing the Shift key.
For unselecting multiple water molecules is exactly the same process: just click the first water molecule of the custom sequence with the mouse left button while pressing the Shift key. A small cross will be shown next to the mouse pointer. Then, click the last water molecule of the custom sequence again with the mouse left button while pressing the Shift key.


Note that multiple selections are only allowed between residues of the same Model and Chain. Trying to select multiple residues from different Model and / or Chain will show an error notification:

IMAGE OF ERROR NOTIFICATION

Trajectories

Each structure can be linked to a trajectory. In this section, initially there is a button that opens a modal window for uploading this trajectory associated with the structure.

Add trajectory

This modal window allows uploading a single trajectory. Note that depending on the file size, the process can take a last. After uploading it to the server it will be processed through MDsrv.

As explained in the introduction, in the backend of this web application is running MDsrv, a powerful tool for viewing and sharing molecular dynamics simulations on the web. So once a trajectory is uploaded, MDsrv processes it in order to stream it frame by frame. 

For further information about MDsrv, please visit the official website or the Nature Methods paper. 

In the 1.0.0. version, only XTC and DCD formats are accepted and the maximum file size is 500MB.


Player
IMAGE OF PLAYER

Once the trajectory has been uploaded and processed in the backend, it can be played through the trajectory player. In this player, trajectories can be played, paused or played manually frame by frame.
Settings
IMAGE OF BLOCK OPEN

This block allows users to modify the trajectory settings.

There is a mini menu at the right side of the block header:
Show tips: opens a modal dialog with a short help for this section.
Show / hide block: allows to open or collapse the panel.

Different trajectory properties can be updated:
Range: initially set from the first to the last frame of the trajectory, defines a range of frames with which the trajectory will be played.
Step: defines the number of frames between playing steps.
Interpolation: type of interpolation between steps. Possible values: None, Linear or Spline.
Loop: if enabled plays the trajectory indefinitely.
Autoplay: if enabled plays the trajectory automatically.

Share
The Share button, located at the top right of the stage, opens a modal window for creating a shared version of the current project.

IMAGE OF SHARED WINDOW

In this window, users must follow three steps:

Draft

Take a look at the project Draft. This Draft is an exact copy of the Shared project so it allows users to figure how the final project will look.

Note that as a draft version of the final Shared page, some of the actions are disabled in this draft page: Embed code, QR code generation and fork project. The rest of the actions are exactly the same as in the final Shared version.

Fork 
Be sure to agree with the fork permissions. Note that once the project is shared, if fork is enabled, every user with the Share representation link will  be able to fork and edit it.

Share
Finally, clicking the Share project button will generate a new read-only project with a different identifier. Once the button is pressed, three new sections will appear in the modal window.

IMAGE OF SHARED WINDOW WITH NEW PROPERTIES

A text box with the new address with a couple of buttons for copying or opening it.
A text box with the embed code. Just copy and paste this code to a new website to embed it.
A QR code that opens the new address.

It’s very important to notice that you can share the same project as many times as you want, but once a project is shared, the subsequent updates in the current representation won't be reflected in the previous shared projects.