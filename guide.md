# Help

## Grig layout

Je definován prvky **row** a **col** a doplňkovou definicí **p1** až **p100** viz příklad použití [code](#code-grid). Před ukončovací značkou **row** je vždy umístěn prvek **clear**.

**Poznámka**
> Pochopitelně není vhodné umisťovat do prvků objekty větší než je definovaná velikost samotného layout prvku **col** v *%*.
> Součet velikostí prvků **col** v **row** by neměl přesáhnout 100 %.

<a name="code-grid"/></a>
**code**
```html
<div class="row">
  <div class="col p10">10%</div>
  <div class="col p20">20%</div>
  <div class="col p30">30%</div>
  <div class="col p40">40%</div>
  <div class="clear"></div>
</div>
<div class="row">
  <div class="col p10">25%</div>
  <div class="col p50">25%</div>
  <div class="col p50">50%</div>
  <div class="clear"></div>
</div>
```
