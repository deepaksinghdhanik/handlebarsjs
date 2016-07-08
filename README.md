## First need to create template
- **type**: "text/x-handlebars-template"
- **id** : define id


    <script id="entry-template" type="text/x-handlebars-template">
      <div class="entry">
        <h1>{{title}}</h1>
        <div class="body">
          {{body}}
        </div>
      </div>
    </script>

## Get template 
    var source   = $("#entry-template").html();

## Complile souce with handlebars.complie method
    var template = Handlebars.compile(source);

## send data into template , it will return compile code with template.
    data =  {title:"This is title", body:"this is body content"};
    console.info(template(data));
    
## for compliling {{{ html }}} tag use triple curly brackets.

## custom helper **Handlebars.registerHelper method**
    <h2>By {{fullName author}}</h2>
    Handlebars.registerHelper('fullName', function(person) {
      return person.firstName + " " + person.lastName;
    });

## Template comments with {{!-- --}} or {{! }}.




