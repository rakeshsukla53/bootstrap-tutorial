# Bootstrap-tutorial

`Bootstrap Themes` You can download themes from here <https://bootswatch.com/>
Download the themes from here, and you just need to replace the css files in the main `css` folder

Most everything that you want to add onto a page by using Bootstrap is done by adding classes and HTML to the page. There are numerous Bootstrap classes. Fortunately, you don't have to know or memorize all of them.

classes are nothing but modifiers for your html content. Once you decide your html content just add appropriate classes.

# Bootstrap Grid System

http://pix.toile-libre.org/?img=1451162165.png

* The grid has 12 columns
* there are four grid systems
     large, medium, small, very small

Grid notes

    Always 12 columns
    Smaller sizes set the default for larger sizes
        col-sm- would set the size for small, medium and large screens unless overridden by a setting specific to one of the larger sizes
    There is a 30px "gutter", or empty space, between each column (15px on each side of the column)
    The gutter on the outside of the container varies based on the current screen size
        Extra small devices always use the entire width of the screen


Grid size classes

Structure of Bootstrap classes for sizing grid content

    col
        Short for column
        Required prefix
    size abbreviation
        xs for Extra small
        sm for Small
        md for Medium
        lg for Large
    Number of columns
        Integer to represent the number of columns

Examples

Let's take a look at a couple of sample Bootstrap content sizing classes:

    col-md-4 would indicate 4 columns for medium and large screens
    col-sm-6 would indicate 6 columns for small, medium and large screens
    col-xs-2 would indicate 2 columns for extra small, medium and large screens

Remember that screen size rules apply for the specified screen size as well as those larger than that size, unless overriden. So the following combination would indicate 2 columns for extra small screens, 6 columns for small screens, and 4 for medium and large screens.

<div class='col-xs-2 col-sm-6 col-md-4'>Content</div>

size between each columns is 15px, there is a size

**if column cannot be contained in one row then it will choose another row**
for example 

<div class="col-md-4">
<div class="col-xs-1">
<div class="col-lg-10">

*<div class="col-md-4"> since here we have not defined any size for small then it will take up all the 12 sizes*


The last one will take up the complete row hence a new row will be selected

**always make sure the column numbers are adding to 12 **

# Bootstrap snippets

Bootstrap snippets are already loaded in my browser and 

`To use the plugin, open an editor, and start typing bs3-, followed by pressing CMD+J. A list of templates will show up. Alternatively, you can type e.g. alert, followed by CMD+J, to immediately show only the alert templates.` 


# Container 

The container class places content inside of a horizontal container. The size of the container will vary based on screensize. The container will stay the same width for that particular screensize. This helps developers size content appropriately for different devices.

fixed width contain

# Container-Fluid

The container-fluid class places content inside of a container that will always be the width of the screen. This is helpful for scenarios where the content to be displayed must use the entire browser window.

not fixed width

# Jumbotran

The jumbotron class is a common class for displaying titles for different sections of a website, or the landing page. The jumbotron typically has a highlighted background and an increased fontsize.

`title` 

# Page Design

Understanding page layout using the `grid system`

n that example, we would have created a section for content that is 6 columns wide, or half of the container. If we then added a new row into that space, replacing the sample content, we'd have a brand new 12 columns. However, those new columns would only take up half of the container, as they are inside of a section that is constraining it to 6 initial columns.

<div class='row'>
  <div class='col-md-6'>
    <div class='row'>
      <!-- 12 new columns here -->
      <!-- This will use half of the container -->
    </div>
  </div>
</div>

**NESTING**

The Bootstrap grid system allows developers to lay out their pages using a system that's similar to tables, but uses CSS positioning instead of tables behind the scenes. One feature tables offer is the ability to create tables inside of a cell, so you can create complex layouts through what's frequently referred to as "nesting". The grid system offers the same capability.

# Controlling Placement

 you can move content to the right 6 columns on extra small screens by using col-xs-push-6. Here are the options available to you:

* offset
        Offset will instruct Bootstrap to skip the specified number of columns before placing content. With offset, the skipped columns will be left blank.
        
  command for offset is
      
    <div class="col-md-4 col-md-offset-3">
       
        
* push
        Push will instruct Bootstrap to move content to the right a specified number of columns. With push, the columns that were left blank can be used by pulling content to the left.
        
* pull
        Pull will instruct Bootstrap to move content to the left a specified number of columns. With pull, the columns that were left blank can be used by pushing content to the right.

We want the display to have LOGO on the right, and DETAILS on the left. So we need to push LOGO over 6, and pull DETAILS over 6. Let's add that in.

    <div class='row'>
       <div class='col-xs-12  col-md-6  col-md-push-6'>LOGO</div>
       <div class='col-xs-12  col-md-6  col-md-pull-6'>DETAILS</div>
    </div>

And the final result will be exactly what we wanted it to be. DETAILS on the left, LOGO on the right for larger displays.


Refer this page for more detals [link](https://courses.edx.org/courses/course-v1:Microsoft+DEV203x+2015_T4/courseware/a8a0655c02d343b59c4e2e3b113665bd/7149ccaa3e1741169b9e6a62bf515be4/)

