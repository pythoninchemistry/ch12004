# The Jupyter Notebook interface

## Interface elements

There are a few sections of the Notebook interface that will be useful to know your way around:

![](images/notebook_interface.png)

1. The jupyterhub logo. Clicking on this takes you back to your **Notebook Dashboard**.
2. The name of your Notebook. Please do not leave this as `Untitled.ipynb`. You will thank me later.
3. Information about when this Notebook was last saved. (or, in Jupyter parlance, when a **checkpoint** was last created.).
    You can force your Notebook to save using:
    - ⌘S (Mac) / alt+S (Windows)
    - Select `File` -> `Save and Checkpoint`.
4. The **Notebook Menubar**. This contains:
    - `File`: File operations, e.g. create a new Notebook, open an existing Notebook, Copy your current Notebook, Save, etc.
    - `Edit`: Manipulating **cells**
    - `View`: Options for what appears on your screen, and for toggling various aspects on and off.
    - `Cell`: Executing one of more **cells**, and manipulating the output of **cells**.
    - `Kernel`: Stop, start, etc. the **kernel**.
    - `Widgets`: Managing plugins and extensions that you might have installed.
    - `Help`: Access to the built-in help.
        - Particularly useful items here are `Help` &#8594; `User Interface Tour` and `Help` &#8594; `Notebook Help`.
5. The **Notebook Toolbar**
    This contains buttons for the most common actions for working with Notebooks. Hovering you mouse over each button will show you a popup with some information about the associated action.
6. The currently selected cell.
7. Indicates whether a cell has run or not, and for cells that have been run, the order they ran in.
8. The text area for the **code cell**. This is where you can type in Pyton code to then run.

## Cells

The body of the notebook is made up of **input cells**. When you open a new notebook it will contain only one empty cell; this is the grey box with `In [  ]:` to the left. 
There are three types of input cells where you can add content to a notebook.

### Code cells

**Code cells** are the default cell type in a notebook.
A **code cell** can accept code, that can then be executed (run). 
When the code in a code cell is run, the notebook displays any output generated by that code directly below the corresponding cell.

![](images/code_cell.png)

In the figure above, the code cell has the Python code `print(4+3)` entered.
This cell has then been [run](heading:running-cells), which executes (runs) the code in the cell: in this instance we add 4 and 3, and print the result.

### Markdown cells

A **markdown cell** contains text formatted using [Markdown](https://www.markdownguide.org/basic-syntax/), which is a lightweight markup language that can be used for writing formatted text. 
When a **markdown cell** is run, the markdown is converted into HTML, with the formatted text then shown _in place_ of the cell.
**Markdown cells** can be used to include formatted text, mathetmatical equations, images, tables, and more types of rich media.

![](images/md_cell.png)
This figure shows a markdown cell being edited, with raw markdown entered.

![](images/formatted_md.png)
This figure shows the same cell after it has been run, with the markdown converted to formatted text.

### Raw cells
Input entered into **Raw cells** is not converted when the cell is run. These cells are usually used to provide additional information for converting Jupyter Notebooks to a different format (e.g., a PDF document). You almost certainly will not need to use **Raw cells** during this course, but might be curious about this third cell type.

### Switching cell type.
Cells can be switched between **code** and **markdown** using the **Cell** &rarr; **Cell Type**  menu options:

![](images/cell_switch.png)

You can also switch between cell types in **commmand mode** (see below) using the keyboard shortcuts `Y` for **code**, `M` for **markdown**, and `R` for **raw**.

### Active cells

A cell is marked as **active** if it is highlighted. The colour of the highlight depends on whether you are in **command mode** or **edit mode**

#### Command mode

**Command mode** is indicated by a blue highlight. When you are in command mode you can use **keyboard shortcuts** to cut, paste, and move cells, etc. You can see all the **keyboard shortcuts** under `Help` &#8594; `Keyboard Shortcuts`.

![](images/command_mode.png)

#### Edit mode

If you are in **command mode** then pressing `Enter` or clicking in the input text area of a cell will switch you to **edit mode**. **Edit mode** is indicated by a green highlight, and a pencil icon in the top right of the Notebook window.

![](images/edit_mode.png)

Typing now inserts text into the currently active cell:

![](images/edit_mode_filled.png)

To get out of **Edit Mode**, and back into **Command Mode**, press `Esc` or click outside the text entry area.

(heading:running-cells)=
## Running cells
Each cell can consist of more than one line of input, which is not processed until the cell is executed, or &ldquo;run&rdquo;.
You can run the currently active cell from the menu bar by clicking **Cell** &rarr; **Run Cells**, or by clicking on the &ldquo;play&rdquo;; icon button in the menu bar.
You can also run the currently selected cell using keyboard shortcuts:
- **ctrl** + **enter**: Run the currently selected cell and keep this cell active.
- **shift** + **enter**: Run the currently selected cell and move the focus to the next cell below. If there is not a cell below, a new empty cell will be created.
- **alt** + **enter** or **option** + **enter**: Run the currently selected cell and create a new empty cell immediately below.

You can also run every cell in a notebook, from top to bottom, by selecting **Kernel** &rarr; **Restart & Run All** from the menu bar. This **halts** your Jupyter notebook and restarts it, before running each cell in sequence from the top down. 