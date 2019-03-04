# Help

* [Grid layout](#section-grid)
* [Buttons](#section-button)
* [Form elements](#section-form)
* [Tooltip](#section-tooltip)
* [SCSS - struktura a členění](#section-scss)
 * Charset
 * Fonts
 * Definice font-family / fonts.google.com.

<a name="section-grid"/></a>
## Grid layout
Je definován prvky DIV s třídami **row** a **col** a doplňkovou třídou **p1** až **p100** viz příklad použití [code](#code-grid). Před ukončovací značkou DIVu **row** je vždy umístěn DIV s třídou **clear**.

**Poznámka**
> Pochopitelně není vhodné umisťovat do prvků objekty větší než je definovaná velikost samotného layout prvku **col** v *%*.
> Součet velikostí prvků **col** v **row** by neměl přesáhnout 100 %, ale menší než 100 % být může.

<a name="code-grid"/></a>
**Code**
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
<a name="section-button"/></a>
## Buttons
Jsou definovány prvky BUTTON, A, INPUT, INPUT[submit] s třídou **button** (kromě BUTTON, tam není základní třída potřeba) a doplňkovými třídami **default**, **submit** a **back** viz příklad použití [code](#code-buttons).

<a name="code-buttons"/></a>
**Code**
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
<a name="section-form"/></a>
## Form elements
Jsou definovány prvky INPUT[radio], INPUT[checkbox], INPUT[text], INPUT[number], INPUT[email], INPUT[password], SELECT, TEXTAREA. Samostatným prvkem je pak SWITCH viz příklad použití [code](#code-forms).

**Poznámka**
> Formulářové prvky je nutné s ohledem na správné formátování obalovat prvky [grid layoutu](#code-grid) viz [příklad](#code-forms-in-grid)

<a name="code-forms"/></a>
**Code**
```html
// Radiobutton inline type
<div class="radio_wrap"> 
  <input type="radio" name="radiobutton" id="labelRadio1"/><span></span><label for="labelRadio1">Label radio button 1</label>
</div>

// Radiobutton block type
<div class="radio_wrap type_block"> 
  <input type="radio" name="radiobutton" id="labelRadio4"/><span></span><label for="labelRadio4">Label radio button 4</label>
</div>

// Checkbox inline type
<div class="check_wrap"> 
  <input type="checkbox" id="labelCheckbox1"/><span></span><label for="labelCheckbox1">Label checkbox button 1</label>
</div>

// Checkbox block type
<div class="check_wrap type_block"> 
  <input type="checkbox" id="labelCheckbox4"/><span></span><label for="labelCheckbox2">Label checkbox button 2</label>
</div>

// Input [text/password/number/email]
<input type="text" />
<input type="number" />
<input type="email" />
<input type="password" />

// Select
<select>
    <option>option 1</option>
</select>

// Textarea
<textarea></textarea>

// Switchbox inline type
<label class="switch_wrap"> 
  <input class="checkbox" type="checkbox">
  <div class="switch"></div>
  <span class="label">Switch 1</span>
</label>

// Switchbox block type
<label class="switch_wrap type_block"> 
  <input class="checkbox" type="checkbox" checked>
  <div class="switch"></div>
  <span class="label">Switch 1</span>
</label>
```

<a name="code-forms-in-grid"/></a>
**Code**
```html
<form action="#">
  <div class="form_block"> // Form container
    <div class="row">
      <div class="col p50">
        <label>Kraj</label> // Standard label
        <select name="region"> // Select
          <option>...</option>
        </select>
      </div>
      <div class="col p50">
        <label>Okres</label>
        <select name="district">  // Select
          <option>Okres ...</option>
        </select>
      </div>
      <div class="clear"></div>
    </div>
    <div class="row">
      <div class="col p50">
        <label class="error">Lorem Ipsum</label>  // Label - state error
        <input class="error" type="text" name="lorem"/> // Input - state error
      </div>
      <div class="col p50">
        <label>Lorem Ipsum</label>
        <input type="text" name="lorem"/>
      </div>
      <div class="clear"></div>
    </div>
    <div class="row">
      <div class="col p100">
        <label>Textarea</label>
        <textarea type="text" name="textarea"></textarea> // Textarea
      </div>
      <div class="clear"></div>
    </div>

    <div class="row">
      <div class="col p50">
        <label>Radiobutton inline type</label>
        <div class="radio_wrap"> // Radiobutton inline type
          <input type="radio" name="radiobutton" id="labelRadio1"/><span></span><label for="labelRadio1">Label radio button 1</label>
        </div>
        <div class="radio_wrap"> // Radiobutton inline type
          <input type="radio" name="radiobutton" id="labelRadio2"/><span></span><label for="labelRadio2">Label radio button 2</label>
        </div>
        <div class="radio_wrap"> // Radiobutton inline type
          <input type="radio" name="radiobutton" id="labelRadio3"/><span></span><label for="labelRadio3">Label radio button 3</label>
        </div>
      </div>
      <div class="col p50">
        <label>Radiobutton block type</label>
        <div class="radio_wrap type_block"> // Radiobutton block type
          <input type="radio" name="radiobutton" id="labelRadio4"/><span></span><label for="labelRadio4">Label radio button 4</label>
        </div>
        <div class="radio_wrap type_block"> // Radiobutton block type
          <input type="radio" name="radiobutton" id="labelRadio5"/><span></span><label for="labelRadio5">Label radio button 5</label>
        </div>
        <div class="radio_wrap type_block"> // Radiobutton block type
          <input type="radio" name="radiobutton" id="labelRadio6"/><span></span><label for="labelRadio6">Label radio button 6</label>
        </div>
      </div>
      <div class="clear"></div>
    </div>
    
    <div class="row">
      <div class="col p50">
        <label>Checkbox inline type</label>
        <div class="check_wrap"> // Checkbox inline type
          <input type="checkbox" id="labelCheckbox1"/><span></span><label for="labelCheckbox1">Label checkbox button 1</label>
        </div>
        <div class="check_wrap"> // Checkbox inline type
          <input type="checkbox" id="labelCheckbox2"/><span></span><label for="labelCheckbox2">Label checkbox button 1</label>
        </div>
        <div class="check_wrap"> // Checkbox inline type
          <input type="checkbox" id="labalCheckbox3"/><span></span><label for="labalCheckbox3">Label checkbox button 1</label>
        </div>
      </div>
      <div class="col p50">
        <label>Checkbox block type</label> 
        <div class="check_wrap type_block"> // Checkbox block type
          <input type="checkbox" id="labelCheckbox4"/><span></span><label for="labelCheckbox4">Label checkbox button 1</label>
        </div>
        <div class="check_wrap type_block"> // Checkbox block type
          <input type="checkbox" id="labelCheckbox5"/><span></span><label for="labelCheckbox5">Label checkbox button 1</label>
        </div>
        <div class="check_wrap type_block"> // Checkbox block type
          <input type="checkbox" id="labalCheckbox6"/><span></span><label for="labalCheckbox6">Label checkbox button 1</label>
        </div>
      </div>
      <div class="clear"></div>
    </div>    

    <div class="row">
      <div class="col p50">
        <label>Switchbox inline type</label>
        <label class="switch_wrap"> // Switchbox inline type
          <input class="checkbox" type="checkbox">
          <div class="switch"></div>
          <span class="label">Switch 1</span>
        </label>
        <label class="switch_wrap"> // Switchbox inline type
          <input class="checkbox" type="checkbox">
          <div class="switch"></div>
          <span class="label">Switch 2</span>
        </label>
        <label class="switch_wrap"> // Switchbox inline type
          <input class="checkbox" type="checkbox" checked>
          <div class="switch"></div>
          <span class="label">Switch 3</span>
        </label>
      </div>
      <div class="col p50">
        <label>Switchbox block type</label>
        <label class="switch_wrap type_block"> // Switchbox block type
          <input class="checkbox" type="checkbox" checked>
          <div class="switch"></div>
          <span class="label">Switch 1</span>
        </label>
        <label class="switch_wrap type_block"> // Switchbox block type
          <input class="checkbox" type="checkbox">
          <div class="switch"></div>
          <span class="label">Switch 2</span>
        </label>
        <label class="switch_wrap type_block"> // Switchbox block type
          <input class="checkbox" type="checkbox">
          <div class="switch"></div>
          <span class="label">Switch 3</span>
        </label>
      </div>
      <div class="clear"></div>
    </div>

    <div class="controls"> 
      <button class="back"><span>Zrušit</span></button> // Button back
      <button class="submit"><span>Odeslat</span></button> // Button submit
    </div>
  </div>
</form>
```
<a name="section-tooltip"/></a>
## Tooltip
Je možné aplikovat na jakémkoli prvku ve struktuře, který obsahuje třídu **tt-top**, **tt-right**, **tt-bottom** nebo **tt-left**. Textový obsah tooltipu je umístěn do atributu **data-tooltip**. Viz příklad použití [code](#code-tooltip).

<a name="code-tooltip"/></a>
**Code**
```html
// Tooltips on Buttons
<button class="tt-top" data-tooltip="Top Tooltip"></button>
<button class="tt-right" data-tooltip="Right Tooltip"></button>
<button class="tt-bottom" data-tooltip="Bottom Tooltip"></button>
<button class="tt-left" data-tooltip="Left Tooltip"></button>

//Tooltips on Links
<a href="#" class="tt-bottom" data-tooltip="Bottom Tooltip"></a>
<a href="#" class="tt-top" data-tooltip="Top Tooltip"></a></p>

...
```
<a name="section-scss"/></a>
## SCSS - struktura a členění

### Charset
Definice znakové sady.

**Code**
```scss
@charset 'utf-8';
```
### Fonts
Definice font-family / fonts.google.com.

**Code**
```scss
@import url('//fonts.googleapis.com/css?family=Nunito:300,300i,400,400i,600,600i,700,700i&subset=latin-ext');
```
### SCSS include / structura komponent SCSS

```scss
@import "g_variables";		 /*Nastaveni globalnich promennych, mixinu,...*/
@import "full_reset";     	 /*Reset vychozich hodnot - globalne*/
@import "core_elements"; 	 /*Obecne prvky - globalne*/
@import "form_elements"; 	 /*Formularove prvky*/
@import "button_elements"; 	 /*Tlacitka*/
@import "grid_elements"; 	 /*Zakladni prvky konstruktu*/
@import "layout_elements";	 /*Layout / HP / SP /...*/
@import "popup_elements";	 /*Popup - dialog*/
@import "tooltip_elements";  /*Tooltipy*/
@import "messages_elements"; /*Message info/alert/error/default*/
```



