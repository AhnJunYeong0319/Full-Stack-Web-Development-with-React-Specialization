## Task 1

In this task you will be adding another content row to the page. The content row should contain the following:

- You should create a reservation form for the user to reserve a table. The reservation form should contain a field using radio that enables the users to specify the number of guests (1-6).

- The form should contain fields to specify the date and time of the reservation. The fields should contain appropriate placeholder information to identify the purpose of the fields.

- The form should contain a button named Reserve to initiate reservation of the table.

- The form should be enclosed inside a card with the heading "Reserve a Table". The card should occupy 8 columns and centred in the row for small to extra-large screens. For extra-small screens, the card should span the entire row.

```html
<!-- Task 1 -->
        <div class = 'row row-content align-items-center'>
            <div class = "col-12 col-sm-8 offset-sm-2">

                <div class="card ">
                    <h3 class="card-header bg-warning text-white">Reserve a Table</h3>
                    <div class="card-body">
        
                        <form id="form">
                            <div class="form-group row">
                                <label class="col-md-2 col-form-label">Number of Guests</label>
                                <div class="col-2 col-md-1">
                                    <div class="form-check form-check-inline">
                                        <input type="radio" class="form-check-input"
                                        name="approve1" id="approve1" value="">
                                        <label class="form-check-label" for="approve1">
                                            1
                                        </label>
                                    </div>
                                </div>
                                <div class="col-2 col-md-1">
                                    <div class="form-check form-check-inline">
                                        <input type="radio" class="form-check-input"
                                        name="approve2" id="approve2" value="">
                                        <label class="form-check-label" for="approve2">
                                            2
                                        </label>
                                    </div>
                                </div>
                                <div class="col-2 col-md-1">
                                    <div class="form-check form-check-inline">
                                        <input type="radio" class="form-check-input"
                                        name="approve3" id="approve3" value="">
                                        <label class="form-check-label" for="approve3">
                                            3
                                        </label>
                                    </div>
                                </div>
                                <div class="col-2 col-md-1">
                                    <div class="form-check form-check-inline">
                                        <input type="radio" class="form-check-input"
                                        name="approve4" id="approve4" value="">
                                        <label class="form-check-label" for="approve4">
                                            4
                                        </label>
                                    </div>
                                </div>
                                <div class="col-2 col-md-1">
                                    <div class="form-check form-check-inline">
                                        <input type="radio" class="form-check-input"
                                        name="approve5" id="approve5" value="">
                                        <label class="form-check-label" for="approve5">
                                            5
                                        </label>
                                    </div>
                                </div>
                                <div class="col-2 col-md-1 mr-1">
                                    <div class="form-check form-check-inline">
                                        <input type="radio" class="form-check-input"
                                        name="approve6" id="approve6" value="">
                                        <label class="form-check-label" for="approve6">
                                            6
                                        </label>
                                    </div>
                                </div>

                                
                            </div>
                            <div class="form-group row">
                                <label for="datetime" class="col-md-2 col-form-label">Date and Time</label>
                                <div class="col-12 col-md-5">
                                    
                                    <input type="text" class="form-control" id="date" name="date"
                                    placeholder="Date">
                                </div>
                                <div class="col-12 col-md-5">
                                
                                    <input type="text" class="form-control" id="time" name="time"
                                    placeholder="Time">
                                </div>
                            </div>
                            <div class="form-group row">
                                <div class="offset-md-2 col-md-10">
                                    <button type="submit" class="btn btn-primary">
                                        Reserve
                                    </button>
                                </div> 
                            </div>

                        </form>
                    </div>
                </div>
            </div>
        </div>
<!-- Task 1 -->
```


<br><br>

## Task 2

In this task you will be formatting the content in the second row of the page. The formatting should result in the following:

- Format the content of the second column with the media class together with the media object class. Use the buffet.png image file provided for you in the img folder. The image should displayed to the right of the content description. See figure below.

- Add a badge with the word “NEW” to the content as shown in the figure below.


```html
<!-- Task 2 -->
    <div class="media">
        
        <div class="media-body">
            <h2>Weekend Grand Buffet <span class="badge badge-danger">NEW</span> </h2>
            <p class="d-none d-sm-block">Featuring mouthwatering combinations with a choice of five different salads, six enticing appetizers, six main entrees and five choicest desserts. Free flowing bubbly and soft drinks. All for just $19.99 per person </p>
        </div>
        <img class="d-flex ml-3 img-thumbnail align-self-center"
        src="img/buffet.png" alt="buffet">
    </div>
<!-- Task 2 -->
```

<br><br>

## Task 3

In this task you will be adding a block-sized button to the Jumbotron to the right of the restaurant logo:


- The block-level button and the restaurant logo should share the right six columns of the row. The restaurant name and description can now be reduced to occupy the left six columns. Use the small button (btn-sm).

- Clicking on the button should take you down to the form for reserving a table.

```html
<!-- Task 3 -->

    <div class = "d-grid gap-2 col-12 col-sm-3 align-self-center text-center"> <!-- if extra small, stacked below - otherwise, occupy the right space of the empty columns-->
        <a class="btn-sm btn-warning btn-block" href="#form" role="button">Reserve Table</a>

    </div>

<!-- Task 3 -->
```