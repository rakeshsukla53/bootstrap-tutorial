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

    <div class="col-md-4"> since here we have not defined any size for small then it will take up all the 12 sizes*
    

The last one will take up the complete row hence a new row will be selected

**always make sure the column numbers are adding to 12**

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

**MOBILE FIRST ALWAYS**

# Controlling Visibility

Bootstrap offers you the ability to show or hide content based on both screen size and printing state. The syntax is, as with much of Bootstrap, option-screen.

The two options are either hidden or visible. Both of the options will change the default for all other screen sizes and print. In other words, `hidden-sm` will make the content hidden for small screens, but visible on all others; `visible-sm` will make the content visible on small screens, but visible on all others.

# Navigation

The `navbar` is a Bootstrap component and is designed to provide navigation for the user. It's most commonly placed at the top of a page.


**Positioning the navbar**

The first option is to have it appear at the top of the page as a normal element, scrolling, and disappearing off the top of the browser window, along with the rest of the content. This is achieved by adding the `navbar-static-top` class.

The second option is affix it to the top of the page, so it will not disappear when the user scrolls, but rather stay in place. This is achieved by adding the `navbar-fixed-top` class.

Finally, you can have the navbar use the same behavior on the bottom of the page with `navbar-fixed-bottom`.

if you are using either fixed option, you are required to add padding to the top (for `navbar-fixed-top`), or bottom (for `navbar-fixed-bottom`) to the body element.

# Tabs

Tabs allow you to display data in different pages, each one with a tab title on top of it. Tabs are perfect for scenarios when you have a lot of data to display, but the user only needs it in smaller chunks, displayed one at a time. One key thing to remember about using tabs is they are restricting the user's ability to scroll.

    Code for it
    

    <ul class="nav nav-tabs" role="tablist">
        <li class="active"><a href="#tab1" role="tab" data-toggle="tab">Tab1</a></li>
        <li><a href="#tab2" role="tab" data-toggle="tab">Tab2</a></li>
        <li><a href="#tab3" role="tab" data-toggle="tab">Tab3</a></li>
    </ul>
    <!-- TAB CONTENT -->
    <div class="tab-content">
        <div class="active tab-pane fade in" id="tab1">
            <h2>Tab1</h2>
            <p>Lorem ipsum.</p>
        </div>
        <div class="tab-pane fade" id="tab2">
            <h2>Tab2</h2>
            <p>Lorem ipsum.</p>
        </div>
        <div class="tab-pane fade" id="tab3">
            <h2>Tab3</h2>
            <p>Lorem ipsum.</p>
        </div>
    </div>

# ScrollSpy 

Scrollspy is a data display that allows a user to jump directly to the data they wish to see, but also enables scrolling. Like tabs, scrollspy provides navigation tabs. But unlike tabs, scrollspy allows a user to scroll through content as well.


    <h2>Scrollspy</h2>
    <div style="position:relative;">
      <!-- Navigation -->
      <nav class="navbar navbar-default navbar-static" role="navigation" id="navbar-spy">
        <ul class="nav navbar-nav">
          <li class="active"><a href="#scroll-first">First</a></li>
          <li><a href="#scroll-second">Second</a></li>
        </ul>
      </nav>
     
      <!-- Content -->
      <div data-target="#navbar-spy" data-spy="scroll" style="height:150px; overflow-y:scroll; position:relative;">
        <div id="scroll-first">
          <!-- first block of content -->
        </div>
        <div id="scroll-second">
          <!-- second block of content -->
        </div>
      </div>
    </div>

# Accordion

The accordion is built using the panel capabilities of Bootstrap. The container will be decorated with the panel-group class. It will also need an ID to represent the accordion container.

    <div class="panel-group" id="accordion-sample">
        <div class="panel panel-default">
            <div class="panel-heading">
                <h4 class="panel-title">
                    <a data-toggle="collapse" data-parent="#accordion-sample" href="#accordion-sample-one">
                        Heading One
                    </a>
                </h4>
            </div>
            <div id="accordion-sample-one" class="panel-collapse collapse in">
                <div class="panel-body">
                    Sample content
                </div>
            </div>
        </div>
        <div class="panel panel-default">
            <div class="panel-heading">
                <h4 class="panel-title">
                    <a data-toggle="collapse" data-parent="#accordion-sample" href="#accordion-sample-two">
                        Heading Two
                    </a>
                </h4>
            </div>
            <div id="accordion-sample-two" class="panel-collapse collapse">
                <div class="panel-body">
                    Sample content
                </div>
            </div>
        </div>
    </div>



# Carousel

A carousel is a paging data display. It's ideal for looping through a group of photos, or potentially advertisements.

    <div id="carousel-demo" class="carousel slide" data-ride="carousel">
       <ol class="carousel-indicators">
         <li data-target="#carousel-demo" data-slide-to="0" class="active"></li>
         <li data-target="#carousel-demo" data-slide-to="1"></li>
       </ol>
       <div class="carousel-inner">
         <div class="item active">
           <img alt="First slide" src="image-url" />
           <div class="carousel-caption">
             <h3>Caption Heading One</h3>
             <p>Caption Text One</p>
           </div>
         </div>
         <div class="item">
           <img alt="Second slide" src="image-url" />
           <div class="carousel-caption">
             <h3>Caption Heading Two</h3>
             <p>Caption Text Two</p>
           </div>
         </div>
       </div>
       <a class="left carousel-control" href="#carousel-demo" data-slide="prev">
         <span class="glyphicon glyphicon-chevron-left"></span>
       </a>
       <a class="right carousel-control" href="#carousel-demo" data-slide="next">
         <span class="glyphicon glyphicon-chevron-right"></span>
       </a>
    </div>

The carousel control is really four parts. The first part is the container for the carousel. Inside of the container, you will create the set of indicators for the current slide, the container for all of the slides, and the navigation to allow the user to change slides.


# Bootstrap forms

Bootstrap offers great support for collecting information from users, as well as providing feedback. As with everything else in Bootstrap, you create forms by adding the appropriate classes and HTML structure to your pages.

    <form class="form-horizontal">
            <div class="form-group">
                <label for="address" class="control-label col-md-3">Address:</label>
                <div class="col-md-6">
                    <input type="text" name="address" id="address" class="form-control" />
                </div>
            </div>
        </form>

HTML5 offers several improvements over the classic HTML controls, including the ability to add placeholders, and support for new data-types, such as email addresses. However, you'll notice that textboxes still look like textboxes. Bootstrap offers the ability to enhance textboxes, providing more inline support and guidance as to the type of data you expect from a user.

    <form class="form-horizontal">
        <div class="form-group">
            <label for="username" class="control-label col-md-3">Username:</label>
            <div class="col-md-6">
                <div class="input-group">
                    <div class="input-group-addon">
                        <span class="glyphicon glyphicon-user"></span>
                    </div>
                    <input type="text" class="form-control" name="username" id="username" />
                </div>
            </div>
        </div>
    </form>

# Buttons 


Modifier	Default color
Default 	White
Primary 	Dark blue
Success 	Green
Info 	    Light blue
Warning 	Yellow
Danger 	    Red


    <form class="form-horizontal">
        <div class="form-group">
            <div class="col-md-offset-3 btn-group" data-toggle="buttons">
                <label class="btn btn-primary">
                    <input type="radio" id="first" name="sample" />
                    First
                </label>
                <label class="btn btn-primary">
                    <input type="radio" id="second" name="sample" />
                    Second
                </label>
            </div>
        </div>
        <div class="form-group">
            <button type="submit" class="btn btn-default col-md-offset-3 col-md-4">Submit form</button>
        </div>
    </form>

# Alerts

    <div class="alert">
        <button type="button" class="close" data-dismiss="alert" aria-hidden="true">&times;</button>
        <strong>Alert</strong> The page is not avialable
    </div>
    
    <div class="alert alert-danger">
        <button type="button" class="close" data-dismiss="alert" aria-hidden="true">&times;</button>
        <strong>Title!</strong> Alert body ...
    </div>
    
    <div class="alert alert-success">
        <button type="button" class="close" data-dismiss="alert" aria-hidden="true">&times;</button>
        <strong>Title!</strong> Alert body ...
    </div>
    
    <div class="alert alert-warning" role="alert">
        <strong>Warning!</strong> Better check yourself, you're <a href="#" class="alert-link">not looking too good</a>.
    </div>
    
    <div class="container">
        <div class="alert alert-warning alert-dismissable">
            <button type="button" class="close" data-dismiss="alert" aria-hidden="true">×</button>
            <h3>Warning</h3>
            <div>It appears that something has gone wrong</div>
        </div>
    </div>


# Modal Dialogs

Modal dialogs are the ultimate way to get the user's attention, as the user can't interact with the rest of the page without first closing the modal dialog. Modal dialogs can contain whatever HTML you need to present, including status messages, videos, or forms.

`bs3-modal`


# Bootstrap Code Snippets

http://www.newthinktank.com/2015/11/learn-bootstrap-one-video/

All snippets are here


# Panel 

A panel in bootstrap is a bordered box with some padding around its content:

# Pagination 

If you have a web site with lots of pages, you may wish to add some sort of pagination to each page.

<ul class="pagination pagination-large">
	<li><a href="#">&laquo;</a></li>
	<li><a href="#">1</a></li>
	<li><a href="#">2</a></li>
	<li><a href="#">3</a></li>
	<li><a href="#">4</a></li>
	<li><a href="#">5</a></li>
	<li><a href="#">&raquo;</a></li>
</ul>

# Google Map

    <div id="googleMap" style="height:400px;width:100%;"></div>
    
        <!-- Add Google Maps -->
        <script src="http://maps.googleapis.com/maps/api/js"></script>
        <script>
            var myCenter = new google.maps.LatLng(41.878114, -87.629798);
    
            function initialize() {
                var mapProp = {
                    center:myCenter,
                    zoom:12,
                    scrollwheel:false,
                    draggable:false,
                    mapTypeId:google.maps.MapTypeId.ROADMAP
                };
    
                var map = new google.maps.Map(document.getElementById("googleMap"),mapProp);
    
                var marker = new google.maps.Marker({
                    position:myCenter,
                });
    
                marker.setMap(map);
            }
    
            google.maps.event.addDomListener(window, 'load', initialize);
        </script>   


# Pager 

    <ul class="pager">
        <li><a href="#">Previous</a></li>
        <li><a href="#">Next</a></li>
    </ul>























