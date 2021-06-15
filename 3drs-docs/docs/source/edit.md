# Edit representation

Once the structure or structures are uploaded, users will be redirected to the **Edit representation page**. This page loads the structure(s) and shows a notification warning that the project will expire unless it’s shared. That means that users have **until the date shown** in the notification for editing and sharing a project. In case of not sharing it after this period of time, all the files and data related to the project will be **removed** from our database.

In the current version, the expiration time is **20 days**.

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

> **Structure file name** | Model **number** | Chain **ID** | **Residue name (Residue long name) Residue number** Atom name (or Bond)

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
* **[Camera type](#camera-type)**
* **[Help](#help)**
* **[Project settings](#project-settings)**

### Reload

![](_static/edit/edit05.png)

Clicking this button **restores the view to the initial position** on the **stage**.

### Center

![](_static/edit/edit06.png)

Clicking this button **centers** the structure(s) position on the **stage**.

### Background

![](_static/edit/edit07.png)

Clicking this button opens a **color picker** that allows users to change the **background color** of the **stage**.

### Full screen

![](_static/edit/edit08.png)

Clicking this button opens the **fullscreen mode**. For **exiting** full screen mode, just **click the button again** or press the **Esc key**.

### Superposition

![](_static/edit/edit09.png)

3dRS allows to **superpose** multiple structures **in pairs**. Clicking the Superposition button **opens a new modal dialog** with a list of **all the structures** present in the project:

![](_static/edit/edit09a.png)

As an example, **3DBQ** and **1U19** are shown before superposition:

![](_static/edit/edit09c.png)

Users must select **two structures** and specify in [NGL viewer Selection Language](https://nglviewer.org/ngl/api/manual/usage/selection-language.html) the **superposition area** of each structure. If Selection field is empty, **all the structure** will be taken as a superposition area.

![](_static/edit/edit09b.png)

After **selecting** and **clicking** the **Apply superposition button**, both structures will be superposed (in the given example, they have been superposed on the A chain):

![](_static/edit/edit09d.png)

Note that this button **only appears in case more than one structure** has been uploaded.

### Measurements

![](_static/edit/edit10.png)

Clicking this button **opens a modal dialog** to edit the **distances and angles** created by users in the stage. For remembering how to draw them, please go back to the **[Mouse click actions section](#mouse-click-actions)**.

**Measurements** with size and color **by default**:

![](_static/edit/edit10a.png)

**Distances** before editing size and color:

![](_static/edit/edit10b.png)

**Distances** after editing size and color:

![](_static/edit/edit10c.png)

**Angles** before editing size and color:

![](_static/edit/edit10d.png)

**Angles** after editing size and color:

![](_static/edit/edit10e.png)

**Measurements** after **size and color edition**:

![](_static/edit/edit10f.png)

In the current version, distances between different structures dont work.

### Navigation mode

![](_static/edit/edit11a.png)

Sometimes it's difficult to move the stage without **accidentally selecting** a residue from it. For the sake of avoiding these problems, a **Navigation mode button** is provided. Clicking it **disables** the **selection** of molecules and the creation of **distances** and **angles**.

Once the button is clicked, it turns out its background to white and the compass icon starts **spinning**:

![](_static/edit/edit11b.png)

During the navigation mode, the mouse pointer changes its aspect to a grabbing hand:

![](_static/edit/edit11c.png)

The **Navigation mode** will be enabled until users **click the button again**.

### Camera type

![](_static/edit/edit12z.png)

Switches camera type between **orthographic** and **perspective**.

### Help

![](_static/edit/edit12.png)

Link to this same [Read the Docs](https://3drs-documentation.readthedocs.io/en/latest).

### Project settings

![](_static/edit/edit13.png)

Clicking this button **opens a modal dialog** to edit the **project settings**:

![](_static/edit/edit13b.png)

* **Project title:** title of the project. If this field is empty, neither title nor caption will be shown in the project once shared
* **Representation caption:** representative information of the project such as description, author(s), links and so on. Beware of copying **formatted text**, it can give problems. It's strongly reccomended to paste text without formatting (via **Ctrl+Shift+V** or **Tx** button).
* **Fork project when shared:** if enabled, the project will be able to be forked once shared. That means that anyone can make an editable copy of the project.
* **Make project public:** if enabled, the project will be shown in the home page list along with the rest of latest public projects.
* **Overlay messages:** there are notification messages for almost each action in the application. With this button they can be enabled / disabled. Note that although this option is enabled, the expiration notification will still appear as well as some error messages and the navigation mode prompt.
* **Creation date:** date of creation of the project.
* **Expiration date:** date of expiration of the project. This date will disappear once the project is shared for the first time, since then the project will be persistent.

## Representations

The **Representations** panel is at the bottom left of the stage and is used for changing the properties of the representation.

Initially, there is a **Default** representation that only allows to change the opacity and hide or show it:

![](_static/edit/edit14a.png)

Once users create a new representation, there are **all the properties** available:

![](_static/edit/edit14b.png)

### Representation actions

Below there is a description of **all the actions** that can be performed in this panel.

#### Select representation

![](_static/edit/edit15.png)

In this dropdown menu, users can switch **between all the representations** of the project.

#### Edit representations

Below the select dropdown menu there is a tiny menu for making **some actions** over the **representations**.

##### Hide / show

![](_static/edit/edit16.png)

**Hides** or **show** the **current representation** selected on the dropdown above.

##### Hierarchy map

![](_static/edit/edit17.png)

Shows a **modal dialog** with all the molecules selected in **each representation**:

![](_static/edit/edit17a.png)

In the default representation this feature is disabled.

##### Edit representation name

![](_static/edit/edit18.png)

Allows to **rename** the **current representation**:

![](_static/edit/edit18a.png)

In the default representation this feature is disabled.

##### Edit label 

![](_static/edit/edit19.png)

Clicking this button opens the **label edition area**:

![](_static/edit/edit19a.png)

**By default**, all the actions are **disabled** until the label is **enabled** clicking the switch button.

Once the label is enabled, it will appear in the **stage** with generic size and color and centered in the current selection. Note that the **default position** varies depending on the structure and the atoms selected. Sometimes the label can be out of the selection or in a **non-representative position**. In order to fix that, a **place label button** is provided (explained below).

**Generic label** aspect:

![](_static/edit/edit19b.png)

In the **label edition area**, users can modify the label **name**, the label **size**, the label **background color** and the label **position**:

![](_static/edit/edit19c.png)

To **modify the label position**, the place label button must be clicked:

![](_static/edit/edit19e.png)

Once the button is clicked, it turns out its background to white and the crosshair icon starts **spinning**:

![](_static/edit/edit19f.png)

During this label position mode is active, the mouse pointer changes its aspect to a **crosshair**:

![](_static/edit/edit19g.png)

Note that during this mode, the **selection** of molecules and the creation of **distances** and **angles** are disabled. Picking a molecule only will translate the label to its position.

**Edited label** aspect:

![](_static/edit/edit19d.png)

In the default representation this feature is disabled.

##### Clone representation

![](_static/edit/edit20.png)

Clicking this button will **duplicate the current representation** with the same features and selection.

In the default representation this feature is disabled.

##### Remove

![](_static/edit/edit21.png)

**Removes** the **current representation and all the selections** linked to it. This button must be clicked **twice** in order to ensure that it has not been clicked by mistake. 

In the default representation this feature is disabled.

### Representation properties

There are several properties that can be modified for each representation.

#### Molecular representation

![](_static/edit/edit22.png)

Each loaded **structure** can be displayed using a variety of **molecular representations**:

##### Backbone

Cylinders connect successive residues of unbroken chains by their main backbone atoms, which are **.CA** atoms in case of proteins and **C4'/C3'** atoms for RNA/DNA, respectively. The main backbone atoms are displayed as spheres.

![](_static/edit/edit23a.png)

##### Ball and stick

Atoms are displayed as spheres (balls) and bonds as cylinders (sticks).

![](_static/edit/edit23b.png)

##### Cartoon

The main backbone atoms (see backbone) of successive residues in unbroken chains are connected by a smooth trace. The trace is expanded perpendicular to its tangent with an elliptical cross-section. The major axis points from **.CA** in the direction of the .O in case of proteins and from the **C1'/C3'** to **C2'/O4'** for RNA/DNA, respectively.

If RNA/DNA an **additional base representation** is added: simplified display of RNA/DNA nucleotides, best used in conjunction with a cartoon representation. Here, a stick is drawn connecting the sugar backbone with a nitrogen in the base (**.N1** in case of adenine or guanine, **.N3** in case of thymine or cytosine).

![](_static/edit/edit23c.png)

##### Hyperball

A derivate of the **[ball+stick](#ball-and-stick)** representation (pioneered by [HyperBalls](http://sourceforge.net/projects/hyperballs/) project) in which atoms are smoothly connected by an elliptic hyperboloid.

![](_static/edit/edit23d.png)

##### Licorice

A variant of the **[ball+stick](#ball-and-stick)** representation where balls and sticks have the same radius.

![](_static/edit/edit23e.png)

##### Line

Bonds are displayed by a flat, unshaded line.

![](_static/edit/edit23f.png)

##### Ribbon

A thin ribbon is displayed along the main backbone trace.

![](_static/edit/edit23g.png)

##### Rope

A rope-like protein fold abstraction well suited for coarse-grained structures. In this representation a tube follows the center points of local axes. The result is similar to what is shown by the [Bendix tool](http://sbcb.bioch.ox.ac.uk/Bendix/).

![](_static/edit/edit23h.png)

##### Spacefill

Atoms are displayed as a set of space-filling spheres.

![](_static/edit/edit23i.png)

##### Surface

Displays the molecular surface and its variants.

![](_static/edit/edit23j.png)

##### Trace

A flat, unshaded line is displayed along the main backbone trace.

![](_static/edit/edit23k.png)

##### Tube

Essentially like **[cartoon](#cartoon)** but with the aspectRatio fixed at a value of 1.0.

![](_static/edit/edit23l.png)


Due to a shortcoming of NGL Viewer, the **cartoon** and **ribbon** representations only can show **four or more** consecutive residues.

The **Default** representation can’t be edited but represents the structure in a standard way:

* Backbone: **Cartoon** representation.
* NA bases (if present): **Base** representation.
* Heteroatoms: **Ball and stick** representation.
* Ions: **Ball and stick** representation.
* Waters: **Ball and stick** representation.

![](_static/edit/edit23m.png)

So take into account that if for example there is an heteroatom with **ATOM** instead of **HETATM** in the PDB file, it won’t be shown in this **Default** representation. 

#### Radius

![](_static/edit/edit24.png)

Through this slider, the **radius** can be modified in the next molecular representations:

* Backbone
* Ball and stick
* Licorice
* Spacefill

#### Color scheme

![](_static/edit/edit25.png)

Each loaded structure can be displayed using a variety of **color schemes**:

##### Atom index

Color by atom index.

![](_static/edit/edit25a.png)

##### B-factor

Color by b-factor.

![](_static/edit/edit25b.png)

##### Chain id

Color by chain id.

![](_static/edit/edit25c.png)

##### Chain index

Color by chain index.

![](_static/edit/edit25c.png)

##### Element

Color by chemical element.

![](_static/edit/edit25e.png)

##### Hydrophobicity

Color by hydrophobicity.

![](_static/edit/edit25f.png)

##### Model index

Color by model index.

![](_static/edit/edit25g.png)

##### Random

Class by random color.

![](_static/edit/edit25h.png)

##### Residue index

Color by residue index.

![](_static/edit/edit25i.png)

##### Residue name

Color by residue name.

![](_static/edit/edit25j.png)

##### Secondary structure

Color by secondary structure.

![](_static/edit/edit25k.png)

##### Uniform

Color by uniform color selected from the color picker that appears at right of the dropdown menu when this option is selected.

![](_static/edit/edit25m.png)

![](_static/edit/edit25l.png)


The colors for the **Default** representation are as follows:

* Backbone: **Secondary structure** color scheme.
* NA bases (if present): **Residue name** color scheme.
* Heteroatoms: **Element** color scheme.
* Ions: **Element** color scheme.
* Waters: **Element** color scheme.

![](_static/edit/edit23m.png)

#### Opacity

![](_static/edit/edit26.png)

Through this slider, the **opacity** of the representation varies. Note that due to an incompatibility of NGL Viewer, opacity in multilayer projects can generate some **issues**. So creating multiple representations with different degrees of opacity can give **non desired outcomes**.

Moreover, if the opacity of a representation is **less than 30** it won’t be possible to select the residues from the stage. Due to a WebGL problem, the threshold for allowing selections from stage is set to **greater than 30**.

### New representation

![](_static/edit/edit27.png)

In this text box, users should insert the name for **creating a new representation**. For the sake to clearly see all the items that can be selected in the representation, **initially a line representation will be shown** (see image below). But at the moment that some molecule is selected, the rest of molecules will **disappear** from the stage. See **[next section](#selections)** for a more detailed description of this behavior.

![](_static/edit/edit23f.png)

## Selections

The **Selections** panel is at the right side of the stage and is used for applying selections to the current representation selected in the **[Representations](#representations)** panel.

Note that if the current representation is the **Default** one, this panel will be disabled. Once users create a new representation, the **Representations** panel will open automatically though it can be closed clicking the open / close button.

When a **new representation** is created, all the items in the stage will be selected by default with a **Line** representation and **Secondary structure** color scheme. The meaning of this is to easily glimpse **all the molecules** contained in the representation. Once the **first molecule** (one of Sequence, Heteroatoms, Ions or Waters) is selected, this one will be the only one selected.

The **Selections** panel is divided into ten parts:

![](_static/edit/edit28.png)

* **[Open / close button](#open-close-button)**
* **[Structures](#structures)**
* **[Custom selection](#custom-selection)**
* **[Models](#models)**
* **[Chains](#chains)**
* **[Sequence](#sequence)**
* **[Heteroatoms](#heteroatoms)**
* **[Ions](#ions)**
* **[Waters](#waters)**
* **[Trajectories](#trajectories)**

### Open / close button

![](_static/edit/edit29.png)

This button, located at the left part of the **Selections** panel, allows to **open or close** it.

In the default representation this feature is disabled.

### Structures

#### Select structure

![](_static/edit/edit30.png)

In this dropdown menu, users can switch between the different structures uploaded in the **[Launch project](launch.html)** page.

Opening the dropdown menu and **passing the mouse** over the structures contained on it will **highlight** them in the stage:

![](_static/edit/edit31.png)

If there is only a **single structure**, this dropdown menu will be disabled:

![](_static/edit/edit32.png)

#### Structures menu

Below the dropdown menu there are a couple of buttons:

##### Center structure

![](_static/edit/edit33.png)

Centers the **stage** view in the currently **selected structure**. Note that if there is only a portion of the structure selected, the view will center around **this portion**.

##### Custom selection / Manual selection

![](_static/edit/edit34.png)

As explained **[later on](#custom-selection)**, advanced users can make custom selections using [NGL viewer Selection Language](https://nglviewer.org/ngl/api/manual/usage/selection-language.html). When custom selection is clicked, **only this panel will be shown** in the molecules part of the **Structures panel**. For coming back to the **manual selection** just click the same button again:

![](_static/edit/edit35.png)

### Custom selection

![](_static/edit/edit36.png)

For accessing this section, the **Custom selection** button of the **Structures menu** must be clicked.

In this block, users can add a custom selection written in [NGL viewer Selection Language](https://nglviewer.org/ngl/api/manual/usage/selection-language.html). Please visit the [Selection language](https://nglviewer.org/ngl/api/manual/usage/selection-language.html) section of the NGL Viewer manual **before starting** with this section.

There is a mini menu at the right side of the block header:

* **Show tips:** ![](_static/edit/edit38.png) opens a modal dialog with a short help for this section
* **Show / hide block:** ![](_static/edit/edit37.png) allows to open or collapse the panel.

Two actions can be performed after writing the custom selection:

#### Save

![](_static/edit/edit42.png)

Clicking this button the **custom selection** is added to the **current representation**.

#### Remove

![](_static/edit/edit41.png)

Clicking this button the **custom selection** is removed from the **current representation**.

Note that **custom selection is not compatible with manual selection**, so even though the selections made in the manual selection section will not be removed, they won’t be visible in the stage. If users want to **restore a previously made manual selection**, just removing the custom selection will do the trick.

### Models

![](_static/edit/edit43.png)

If the selected structure has **more than one model**, this block will be enabled allowing users to **switch between the different models** of the structure.

Same heteroatom in **different models** represented in three different colors:

![](_static/edit/edit44.png)

There is a mini menu at the right side of the block header:

* **Show tips:** ![](_static/edit/edit38.png) opens a modal dialog with a short help for this section
* **Show / hide block:** ![](_static/edit/edit37.png) allows to open or collapse the panel.

Note that **switching between models will change the succeeding panels** (i.e. if the Model 1 has two chains A and B and the Model 2 has three chains A, B and C, the Chains block will change).

If there is only a **single model**, this block menu will be disabled:

![](_static/edit/edit45.png)

### Chains

![](_static/edit/edit46.png)

If the selected model of the current structure has **more than one chain**, this block will be enabled allowing users to **switch between the different models** of the structure.

Two **different chains** represented in two different colors:

![](_static/edit/edit47.png)

There is a mini menu at the right side of the block header:

* **Show tips:** ![](_static/edit/edit38.png) opens a modal dialog with a short help for this section
* **Show / hide block:** ![](_static/edit/edit37.png) allows to open or collapse the panel.

Opening the dropdown menu and **passing the mouse** over the chains contained on it will highlight them in the stage:

![](_static/edit/edit48.png)

Note that if the structure has **no chains**, all the molecules will be automatically assigned to the **Chain A**. If the structure has **one or more chains** but some of its molecules have **no chain**, these “orphan” molecules will be assigned to a **mock Chain @**.

If there is only a single chain, this block menu will be disabled:

![](_static/edit/edit49.png)

### Sequence

There are **two ways** to perform sequence residues selection: directly through **[the block in the Selection panel](#selection-panel-block)** or though the **[Zoom window](#zoom-window)**:

#### Selection panel block

![](_static/edit/edit50.png)

This block shows **all the residues of the structure** classified by chains.

There is a mini menu at the right side of the block header:

* **Open / close external window:** ![](_static/edit/edit40.png) allows to open or close the Zoom window for this section.
* **Select / unselect all:** ![](_static/edit/edit39.png) allows to select or unselect all the molecules of this block with a single click.
* **Show tips:** ![](_static/edit/edit38.png) opens a modal dialog with a short help for this section
* **Show / hide block:** ![](_static/edit/edit37.png) allows to open or collapse the panel.

Different actions can be performed with the residues:

##### Highlight

Passing the **mouse over** a residue will **highlight it** on the stage:

![](_static/edit/edit51.png)

##### Selection

**Clicking on a residue** will select it in the current selection **applying to it** the molecular representation, radius, color scheme and opacity selected in the representations panel for the **current representation**:

![](_static/edit/edit52.png)

##### Unselection

**Clicking on a selected residue** will unselect it from the current selection.

##### Zoom

**Clicking on a residue** with the mouse **left button while pressing the Alt key** will do a zoom to the residue:

![](_static/edit/edit52b.png)

##### Multiple selection

For **selecting multiple residues** just click the first residue of the custom sequence with the mouse **left button while pressing the Shift key**. A small cross will be shown next to the mouse pointer:

![](_static/edit/edit54.png)

Then, click the last residue of the custom sequence again with the mouse **left button while pressing the Shift key**:

![](_static/edit/edit53.png)

##### Multiple unselection

For **unselecting multiple residues** is exactly the same process: just click the first residue of the custom sequence with the mouse **left button while pressing the Shift key**. A small cross will be shown next to the mouse pointer:

![](_static/edit/edit54.png)

Then, click the last residue of the custom sequence again with the mouse **left button while pressing the Shift key**.

Note that **multiple selections** are only **allowed** between residues of the **same Model and Chain**. Trying to select multiple residues from **different Model and / or Chain** will show an **error notification**:

![](_static/edit/edit55.png)

If there are **no residues** in the selected structure (i.e. an heteroatom), this block menu will be disabled:

![](_static/edit/edit56.png)

#### Zoom window

![](_static/edit/edit57.png)

This window shows the same information of the **[Sequences block](#selection-panel-block)** but in a little more detail, adding the **ability** of selecting **α-helices** and **β-sheets** if they are present in the structure.

There is a mini menu at the right side of the window:

* **Select / unselect all:** ![](_static/edit/edit59.png) allows to select or unselect all the molecules of this block with a single click.
* **Close window:** ![](_static/edit/edit58.png) closes the window.

Different actions can be performed with the residues:

##### Residue highlight

Passing the **mouse over** a residue will **highlight** it in the stage:

![](_static/edit/edit60.png)

##### Residue selection

**Clicking on a residue** will select it in the current selection **applying to** it the molecular representation, radius, color scheme and opacity selected in the representations panel for the **current representation**:

![](_static/edit/edit61.png)

##### Residue unselection

**Clicking on a selected residue** will **unselect** it from the current selection.

##### Residue zoom

**Clicking on a residue** with the mouse **left button while pressing the Alt key** will do a zoom to the residue:

![](_static/edit/edit61b.png)

##### Multiple residue selection

For **selecting multiple residues** just click the first residue of the custom sequence with the mouse **left button while pressing the Shift key**. A small cross will be shown next to the mouse pointer:

![](_static/edit/edit54.png) 

Then, click the last residue of the custom sequence again with the mouse **left button while pressing the Shift key**:

![](_static/edit/edit62.png)

##### Multiple residue unselection

For **unselecting multiple residues** is exactly the same process: just click the first residue of the custom sequence with the mouse **left button while pressing the Shift key**. A small cross will be shown next to the mouse pointer:

![](_static/edit/edit54.png) 

Then, click the last residue of the custom sequence again with the mouse **left button while pressing the Shift key**.

##### α-helix / β-sheet highlight

Passing the **mouse over** an α-helix or a β-sheet will **highlight it** in the stage:

![](_static/edit/edit63.png)

##### α-helix / β-sheet selection

**Clicking on a α-helix or a β-sheet** will select it in the current selection **applying to it** the molecular representation, radius, color scheme and opacity selected in the representations panel for the **current representation**:

![](_static/edit/edit64.png)

##### α-helix / β-sheet unselection

**Clicking on a selected α-helix or a β-sheet** will **unselect** it from the current selection. Note that to unselect a **whole α-helix or β-sheet** all its residues must be selected.

##### α-helix / β-sheet zoom

* **Clicking on a α-helix or a β-sheet** with the mouse **left button while pressing the Alt key** will do a zoom to the ensemble of residues:

![](_static/edit/edit64b.png)

Note that **multiple selections** are only **allowed** between residues of the **same Model and Chain**. Trying to select multiple residues from **different Model and / or Chain** will show an **error notification**:

![](_static/edit/edit55.png)

### Heteroatoms

![](_static/edit/edit65.png)

This block shows **all the heteroatoms of the structure**.

There is a mini menu at the right side of the block header:

* **Select / unselect all:** ![](_static/edit/edit39.png) allows to select or unselect all the molecules of this block with a single click.
* **Show tips:** ![](_static/edit/edit38.png) opens a modal dialog with a short help for this section
* **Show / hide block:** ![](_static/edit/edit37.png) allows to open or collapse the panel.

There is a **search box** on the top of the heteroatoms list that allows users to perform **searches** on this list.

Different actions can be performed with the heteroatoms:

#### Highlight

Passing the **mouse over** an heteroatom will **highlight** it in the stage:

![](_static/edit/edit66.png)

#### Selection

**Clicking on an heteroatom** will select it in the current selection **applying to it** the molecular representation, radius, color scheme and opacity selected in the representations panel for the **current representation**:

![](_static/edit/edit67.png)

#### Unselection

**Clicking on a selected heteroatom** will **unselect** it from the current selection.

#### Zoom

**Clicking on the Center button** ![](_static/edit/edit68b.png) of each heteroatom will do a zoom on it:

![](_static/edit/edit68.png)

If there are **no heteroatoms** in the selected structure, this block menu will be disabled:

![](_static/edit/edit69.png)

### Ions

![](_static/edit/edit70.png)

This block shows **all the ions of the structure**.

There is a mini menu at the right side of the block header:

* **Select / unselect all:** ![](_static/edit/edit39.png) allows to select or unselect all the molecules of this block with a single click.
* **Show tips:** ![](_static/edit/edit38.png) opens a modal dialog with a short help for this section
* **Show / hide block:** ![](_static/edit/edit37.png) allows to open or collapse the panel.

There is a **search box** on the top of the ions list that allows users to perform **searches** on this list.

Different actions can be performed with the ions:

#### Highlight

Passing the **mouse over** an ion will **highlight it** in the stage:

![](_static/edit/edit71.png)

#### Selection

**Clicking on an ion** will select it in the current selection **applying to it** the molecular representation, radius, color scheme and opacity selected in the representations panel for the **current representation**:

![](_static/edit/edit72.png)

#### Unselection

**Clicking on a selected ion** will **unselect** it from the current selection.

#### Zoom

**Clicking on the Center button** of each ion will do a zoom on it:
![](_static/edit/edit73.png)
 
If there are **no ions** in the selected structure, this block menu will be disabled:

![](_static/edit/edit74.png)

### Waters

There are **two ways** to perform sequence waters selection: directly through **[the block in the Selection panel](#id2)** or though the **[Zoom window](#id3)**:

#### Selection panel block

![](_static/edit/edit75.png)

This block shows **all the waters of the structure** classified by chains.

There is a mini menu at the right side of the block header:

* **Open / close external window:** ![](_static/edit/edit40.png) allows to open or close the Zoom window for this section.
* **Select / unselect all:** ![](_static/edit/edit39.png) allows to select or unselect all the molecules of this block with a single click.
* **Show tips:** ![](_static/edit/edit38.png) opens a modal dialog with a short help for this section
* **Show / hide block:** ![](_static/edit/edit37.png) allows to open or collapse the panel.

Different actions can be performed with the water molecules:

##### Highlight

Passing the **mouse over** a water molecule will **highlight it** on the stage:

![](_static/edit/edit76.png)

##### Selection

**Clicking on a water molecule** will select it in the current selection **applying to it** the molecular representation, radius, color scheme and opacity selected in the representations panel for the **current representation**:

![](_static/edit/edit77.png)

##### Unselection

**Clicking on a selected water molecule** will **unselect** it from the current selection.

##### Zoom

**Clicking on a water molecule** with the mouse **left button while pressing the Alt key** will do a zoom to the water molecule:

![](_static/edit/edit79.png)

##### Multiple selection

For **selecting multiple water molecules** just click the first water molecule of the custom sequence with the mouse **left button while pressing the Shift key**. A small cross will be shown next to the mouse pointer:

![](_static/edit/edit54.png)

Then, click the last water molecule of the custom sequence again with the mouse **left button while pressing the Shift key**:

![](_static/edit/edit78.png)

##### Multiple unselection

For **unselecting multiple water molecules** is exactly the same process: just click the first water molecule of the custom sequence with the mouse **left button while pressing the Shift key**. A small cross will be shown next to the mouse pointer:

![](_static/edit/edit54.png)

Then, click the last water molecule of the custom sequence again with the mouse **left button while pressing the Shift key**.

Note that **multiple selections** are only **allowed** between water molecules of the **same Model and Chain**. Trying to select multiple water molecules from **different Model and / or Chain** will show an **error notification**:

![](_static/edit/edit55.png)

If there are **no water molecules** in the selected structure, this block menu will be disabled:

![](_static/edit/edit80.png)

#### Zoom window

![](_static/edit/edit81a.png)

This window shows the same information of the [**Waters block**](#id2) but in a little more detail.

There is a mini menu at the right side of the window:

* **Select / unselect all:** ![](_static/edit/edit59.png) allows to select or unselect all the molecules of this block with a single click.
* **Close window:** ![](_static/edit/edit58.png) closes the window.

The actions that can be performed are the same that in the **Waters block**:

##### Highlight

Passing the **mouse over** a water molecule will **highlight it** on the stage:

![](_static/edit/edit76.png)

##### Selection

**Clicking on a water molecule** will select it in the current selection **applying to it** the molecular representation, radius, color scheme and opacity selected in the representations panel for the **current representation**:

![](_static/edit/edit77.png)

##### Unselection

**Clicking on a selected water molecule** will **unselect** it from the current selection.

##### Zoom

**Clicking on a water molecule** with the mouse **left button while pressing the Alt key** will do a zoom to the water molecule:

![](_static/edit/edit79.png)

##### Multiple selection

For **selecting multiple water molecules** just click the first water molecule of the custom sequence with the mouse **left button while pressing the Shift key**. A small cross will be shown next to the mouse pointer:

![](_static/edit/edit54.png)

Then, click the last water molecule of the custom sequence again with the mouse **left button while pressing the Shift key**:

![](_static/edit/edit78.png)

##### Multiple unselection

For **unselecting multiple water molecules** is exactly the same process: just click the first water molecule of the custom sequence with the mouse **left button while pressing the Shift key**. A small cross will be shown next to the mouse pointer:

![](_static/edit/edit54.png)

Then, click the last water molecule of the custom sequence again with the mouse **left button while pressing the Shift key**.

Note that **multiple selections** are only **allowed** between water molecules of the **same Model and Chain**. Trying to select multiple water molecules from **different Model and / or Chain** will show an **error notification**:

![](_static/edit/edit55.png)

### Trajectories

Each structure can be linked to a **trajectory**. In this section, initially there is a button that opens a modal window for uploading this **trajectory** associated with the structure.

#### Add trajectory

Clicking the button **Add trajectory** will open the modal window for uploading a trajectory:

![](_static/edit/edit85.png)

![](_static/edit/edit86.png)

This modal window allows **uploading a single trajectory**. Note that depending on the file size, **the process may take a while**. After uploading it to the server it will be processed through **MDsrv**.

As explained in the introduction, in the backend of this web application is running **MDsrv**, a powerful tool for viewing and sharing **molecular dynamics simulations** on the web. So once a trajectory is uploaded, MDsrv processes it in order to **stream it frame by frame**. 

For further information about **MDsrv**, please visit the [official website](https://nglviewer.org/mdsrv) or the [Nature Methods paper](https://doi.org/10.1038/nmeth.4497). 

In the current version, only **XTC**, **DCD**, **TRR**, **BINPOS** and **NETCDF** (.netcdf / .nc) formats are accepted and the maximum file size is **500MB**.

#### Player

![](_static/edit/edit87.png)

Once the trajectory has been **uploaded and processed** in the backend, it can be played through the **trajectory player**. In this player, trajectories can be **played**, **paused** or played manually either **frame by frame** or **dragging the slider**.

#### Settings

![](_static/edit/edit88.png)

This block allows users to modify the **trajectory settings**.

There is a mini menu at the right side of the block header:

* **Show tips:** ![](_static/edit/edit38.png) opens a modal dialog with a short help for this section
* **Show / hide block:** ![](_static/edit/edit37.png) allows to open or collapse the panel.

Different trajectory properties can be updated:

* **Range:** initially set from the first to the last frame of the trajectory, defines a **range of frames** with which the trajectory will be played.
* **Step:** defines the number of frames between playing steps.
* **Interpolation:** type of interpolation between steps. Possible values: None, Linear or Spline.
* **Timeout:** timeout between playing frames. Actually this slider is in a logarithmic scale from **50** to **10000** milliseconds, but it has been set from 0 to 100 for the sake of simplicity.
* **Loop:** if enabled plays the trajectory indefinitely.
* **Autoplay:** if enabled plays the trajectory automatically.
* **Bounce:** if enabled plays in rock / bounce mode (back and forth).

## Share

![](_static/edit/edit90.png)

The **Share button**, located at the top right of the **stage**, opens a modal window for creating a shared version of the current project.

![](_static/edit/edit89.png)

In this window, users must follow four steps:

### Draft

Take a look at the **project Draft**. This Draft is an exact copy of the **Shared project** so it allows users to figure how the final project will look.

Note that as a **draft version** of the final **Shared page**, some of the actions are **disabled** in this draft page: **Embed code, QR code** generation and **fork project**. The rest of the actions are **exactly the same** as in the final Shared version.

### Fork 

Be sure to agree with the **fork permissions**. Note that once the project is shared, if fork is enabled, every user with the Share representation link **will be able to fork and edit it**.

### Public 

Be sure to agree with the **public permissions**. Note that once the project is shared, if public is enabled, the shared project will be available from the Last projects list in the home page.

### Share

Finally, clicking the **Share project button** will generate a new read-only project with a different identifier. Once the button is pressed, **three new sections** will appear in the modal window.

![](_static/edit/edit91.png)

* A text box with the **new address** with a couple of buttons for copying or opening it.
* A text box with the **embed code**. Just copy and paste this code to a new website to embed it.
* A **QR code** that opens the new address.

It’s very important to notice that **you can share the same project as many times as you want**, but once a project is shared, the subsequent updates in the current representation **won't be reflected** in the previous shared projects.