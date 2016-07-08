//get template 
var source   = $("#entry-template").html();
var template = Handlebars.compile(source);
data =  {title:"This is title", body:"this is body content"};
console.info(template(data));
