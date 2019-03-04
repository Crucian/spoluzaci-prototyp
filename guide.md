# Help

## Grid layout
Je definován prvky DIV s třídami **row** a **col** a doplňkovou třídou **p1** až **p100** viz příklad použití [code](#code-grid). Před ukončovací značkou DIVu **row** je vždy umístěn DIV s třídou **clear**.

**Poznámka**
> Pochopitelně není vhodné umisťovat do prvků objekty větší než je definovaná velikost samotného layout prvku **col** v *%*.
> Součet velikostí prvků **col** v **row** by neměl přesáhnout 100 %, ale menší než 100 % být může.

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
## Buttons
Jsou definovány prvky BUTTON, A, INPUT, INPUT[submit] s třídou **button** (kromě BUTTON, tam není základní třída potřeba) a doplňkovými třídami **default**, **submit** a **back** viz příklad použití [code](#code-buttons).

<a name="code-buttons"/></a>
**code**
```html


<button class="default"><span>Default</button>
<button class="submit"><span>Submit</button>
<button class="back"><span>Back</button>

// Link like Button  
<a href="" class="button default"><span>Default</span></a>
<a href="" class="button submit"><span>Submit</span></a>
<a href="" class="button back"><span>Back</span></a>

// Input [button] like Button   
<input type="button" class="button default" value="Default"/>
<input type="button" class="button submit" value="Submit"/>
<input type="button" class="button back" value="Back"/>
  
// Input [submit] like Button  

<input type="submit" class="button default" value="Default"/>
<input type="submit" class="button submit" value="Submit"/>
<input type="submit" class="button back" value="Back"/>
```

