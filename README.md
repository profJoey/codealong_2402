# codealong_2402
<!-- Just an intro --> 
{
    Each topic could be its own course
    Goal is to make you familiar
    Your project will guide where you deepen
}
<!-- Test comment --> 
{
    More than one way to achieve your goal
    Depends on context and preference

}
<!-- box model --> 
{
    <!DOCTYPE html>
    <html>
        <head></head>
        <body></body>
    </html>
    Every element in web design is a rectangle
    Even elements that don't look like it (circle, text)
    Size calculated by width and height
    Width = width + padding-left + padding-right + border-left + border-right
    Height = height + padding-top + padding-bottom + border-top + border-bottom
    The body only has default stylings
    <style>
       body {
        width: auto;
        margin: 5px;
        padding: 5px;
        border: 1px solid red;
        background-color: lightblue;
        }
    </style>
}
<!-- border box / calc() -->
{
    default width is auto, as wide as viewport
    default heigh is auto, fits to content
    let's say I want me page to take up full screen
    [adjust browser screen to show pixel height]
      <style>
    body {
        height: 923px;
    }
    </style>
    But what if we change the screen size?
    We can't predict our user's screen size
    So we can use relative units
    Relative units are based on something that changes
    Example of relative unit is viewport height (vh)
    <style>
    body {
        height: 100vh;
    }
    </style>
    But the height goes beyond the viewport
    To ensure that the elements width/height include padding/border
    <style>
    body {
        box-sizing: border-box;
    }
    </style>
    <style>
    body {
        height: calc(100vh - 10px);
    }
    </style>
}
<!-- flow layout -->
{   
    now we have a webpage whose body will take up the full width and height of our viewport
    so let's put some elements inside the body
    <header></header>        
    <nav></nav>
    <section>1</section>
    <section>2</section>
    <section>3</section>
    <section>4</section>
    <footer></footer>
    so we have thesse 7 elements, but we can't see them
    they don't have any height
    if we put something inside, they would grow to fit the content
    instead, let's give them an explicit height
    and a background color so we can see each element
    <style>
        main > * {
            height: 200px;
            margin: 1rem;
            background-color: orange;
        }
    </style>
    you can see that each element is stacked on top of eachother
    and takes the full wdith minus the margins
    this is a default behavior called the Flow model
    Flow model just means that all block level element stack on top
    and take the full width
    Block level elements as opposed to inline elements
    Most elements you would think of that create any kind of areas on our page are block level
}
<!-- centering a div -->
{
    
}

<!-- Inline Elements -->
{
    Ok, let's make our nav look a bit more like a nav
    We'll add links
    <a href="">Home</a>
    <a href="">About</a>
    <a href="">Play</a>
    The 'a' tag creates a link
    the 'href' is where you want the link to go
    For now we'll leave that blank
    And between the two tags, we put our label
    you can see that by default links don't stack ontop of eachother
    That's because links are examples of inline elements
    Text, spans are inline elements
    Inline elements default flow is to flow from right to left
    But I want this to look a bit better, so...
    <style>
        nav {
            height: auto;
        }
    </style>
    Changing the height to auto will mean the height will be based on the content inside
    This is what I want because I want the height based on the navigation links
    But I want a but more breathing room so I'll add padding
    <style>
        nav {
            height: auto;
        }
    </style>
    I am using a nother relative unit, rem, which is based on text size
    1 rem is the size of the root text size of the page
    this might be more elegant than specific pixels because
    in different screen sizes the font will be bigger or smaller
    so my padding will adjust proportionately
    okay but now I don't want my links crunches wll the way to the left
    i want them nice and centered
    <style>
        nav {
            display: flex;
            justify-content: center;
        }
    </style>

}
<!-- CSS Grid --> {
    rows and columns
    display: grid
    default = 1 column; 1 row / child
    
}
