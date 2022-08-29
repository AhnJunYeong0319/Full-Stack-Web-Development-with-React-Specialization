## Task 1

In this task you will be updating the aboutus.html page to make use of the Bootstrap classes and components:

- Update the page to make use of the Bootstrap CSS classes.

- Update the page to also use your custom styles defined in your styles.css file, and

- Update the page to make use of all the Bootstrap JS components.

```html
<!-- Task 1 -->

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.min.css">
    <link rel="stylesheet" href="css/styles.css">

    <!-- jQuery first, then Popper.js, then Bootstrap JS. -->
    <script src="node_modules/jquery/dist/jquery.slim.min.js"></script>
    <script src="node_modules/popper.js/dist/umd/popper.min.js"></script>
    <script src="node_modules/bootstrap/dist/js/bootstrap.min.js"></script>

<!-- Task 1 -->
```


<br><br>

## Task 2

In this task you will be adding appropriate formatting to the web page contents using container, row and column classes using the Bootstrap grid so that the web page is formatted to look like the figure given below. 

- The "About Us" title should stretch the entire width of the row. 

- The "Our History" part should occupy only half the width of the row for small to extra large screens, leaving space on the right side for more content to be added later. The content should be stacked for extra small screens.

- The "Corporate Leadership" section should stretch the entire width of the row.

```html
<!-- Task 2 -->

<div class = "container">
        <!-- "About Us" title stretchs the entire width of the row. -->
        <div class = "row">
            <div class = "col-12">
               <h3>About Us</h3>
               <hr>
            </div>
        </div>

        <!-- "Our History" occupies only half the width of the row for small to extra large screens and is stacked for extra small screens. -->
        <div class = "row row-content align-items-center">
            <div class = "col-12 col-sm-6">
                <h2>Our History</h2>
                <p>Started in 2010, Ristorante con Fusion quickly established itself as a culinary icon par excellence in Hong Kong. With its unique brand of world fusion cuisine that can be found nowhere else, it enjoys patronage from the A-list clientele in Hong Kong.  Featuring four of the best three-star Michelin chefs in the world, you never know what will arrive on your plate the next time you visit us.</p>
                <p>The restaurant traces its humble beginnings to <em>The Frying Pan</em>, a successful chain started by our CEO, Mr. Peter Pan, that featured for the first time the world's best cuisines in a pan.</p>
            </div>
            <div>
            </div>
        </div>

        <!-- "Corporate Leadership" stretchs the entire width of the row. -->
        <div class = "row row-content align-items-center">
            <div class = "col-12">
                <h2>Corporate Leadership</h2>
</div>

<!-- Task 2 -->
```

<br><br>

## Task 3

In this task you will use some responsive utilities provided by Bootstrap to hide some of the content only for extra small screens. You will make use of the d-none and d-sm-block CSS classes provided by Bootstrap. To understand how to use these classes, please read the documentation here (in particular see how the combination of classes shown here enables you to hide the content for xs screen sizes) to learn how to apply the d-none and d-sm-block classes. This will get you into the habit of consulting the Bootstrap documentation whenever you need to learn more about the various components and classes of Bootstrap. You should apply the classes so that the &lt;p&gt; elements containing the detailed descriptions of the corporate leadership is hidden only for extra small screens. Thus, your page should look like the figure below on extra small screens.

```html
<!-- Task 3 -->

        <div class = "row row-content align-items-center">
            <div class = "col-12">
                <h2>Corporate Leadership</h2>
                <h3>Peter Pan <small>Chief Epicurious Officer</small></h3>

                <!-- "d-none d-sm-block" class -->
                <p class="d-none d-sm-block">Our CEO, Peter, credits his hardworking East Asian immigrant parents who undertook the arduous journey to the shores of America with the intention of giving their children the best future. His mother's wizardy in the kitchen whipping up the tastiest dishes with whatever is available inexpensively at the supermarket, was his first inspiration to create the fusion cuisines for which <em>The Frying Pan</em> became well known. He brings his zeal for fusion cuisines to this restaurant, pioneering cross-cultural culinary connections.</p>
                <h3>Dhanasekaran Witherspoon <small>Chief Food Officer</small></h3>

                <!-- "d-none d-sm-block" class -->
                <p class="d-none d-sm-block">Our CFO, Danny, as he is affectionately referred to by his colleagues, comes from a long established family tradition in farming and produce. His experiences growing up on a farm in the Australian outback gave him great appreciation for varieties of food sources. As he puts it in his own words, <em>Everything that runs, wins, and everything that stays, pays!</em></p>
                <h3>Agumbe Tang <small>Chief Taste Officer</small></h3>

                <!-- "d-none d-sm-block" class -->
                <p class="d-none d-sm-block">Blessed with the most discerning gustatory sense, Agumbe, our CTO, personally ensures that every dish that we serve meets his exacting tastes. Our chefs dread the tongue lashing that ensues if their dish does not meet his exacting standards. He lives by his motto, <em>You click only if you survive my lick.</em></p>
                <h3>Alberto Somayya <small>Executive Chef</small></h3>

                <!-- "d-none d-sm-block" class -->
                <p class="d-none d-sm-block">Award winning three-star Michelin chef with wide International experience having worked closely with whos-who in the culinary world, he specializes in creating mouthwatering Indo-Italian fusion experiences. He says, <em>Put together the cuisines from the two craziest cultures, and you get a winning hit! Amma Mia!</em></p>
            </div>
       </div>

<!-- Task 3 -->
```