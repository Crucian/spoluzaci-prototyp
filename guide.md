# Help

## Grig layout

Je definován prvky **row** a **col** a doplňkovou definicí **p1** až **p100** viz příklad použití [link](#code):
Před ukončovací značkou DIVu **row** je vždy umístěn prvek **clear**.

**Poznámka**
> Pochopitelně není vhodné umisťovat do prvků objekty větší než je definovaná velikost samotného layout prvku **col** v *%*.
> Součet velikostí prvků **col** v **row** by neměl přesáhnout 100 %.

<a name="code-grid"/></a>
**code**
```html
<div class="row">
  <div class="col p1">1%</div>
  <div class="col p2">2%</div>
  <div class="col p3">3%</div>
  <div class="col p4">4%</div>
  <div class="col p4">4%</div>
  <div class="col p4">4%</div>
  <div class="col p4">4%</div>
  <div class="col p4">4%</div>
  <div class="col p4">4%</div>
  <div class="col p4">4%</div>
  <div class="col p4">4%</div>  
  <div class="col p10">10%</div>
  <div class="col p10">10%</div>
  <div class="col p10">10%</div>
  <div class="col p10">10%</div>
  <div class="col p10">10%</div>
  <div class="col p10">10%</div>
  <div class="col p10">10%</div>
  <div class="col p10">10%</div>
  <div class="clear"></div>
</div>
```


<div class="row">
    <div class="col p1">1%</div>
    <div class="col p2">2%</div>
    <div class="col p3">10%</div>
    <div class="col p10">10%</div>
    <div class="col p10">10%</div>
    <div class="col p10">10%</div>
    <div class="col p10">10%</div>
    <div class="col p10">10%</div>
    <div class="col p10">10%</div>
    <div class="col p10">10%</div>
    <div class="col p10">10%</div>
    <div class="clear"></div>
</div>

<div class="col p14">14%</div>

</body>
</html>


```html
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
