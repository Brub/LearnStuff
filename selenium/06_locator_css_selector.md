# CSS selector locator
CSS Selector is best option if web element has no ID and name. CSS is faster than XPath. CSS is more readable than XPath. It also improves the performance. It is very compatible across browsers. It is very useful when we want to test our application on multiple browsers because CSS engine are consistent in all browsers. CSS is best for IE as XPath does not work in IE always.

## Examples:
### CSS Selectors by Element type
Here you can use the different tagnames (p, div, span, input, a, button, form, h1, img, table, ...)  
In python test code

```
driver.find_element(By.CSS_SELECTOR, "input")
``` 

---
### CSS Selectors by Attribute
```
<input type="text" id="fistname" name="first_name" class="myForm">
```

In python test code

```
driver.find_element(By.CSS_SELECTOR, "[name='first_name']")
driver.find_element(By.CSS_SELECTOR, "[type='text']")
``` 
#### attribute starts with
here you need to use the ^
```
<img scr="images/img1.jpg" alt="vscode run python script"> ✅
<img scr="images/img2.jpg" alt="usage of vscode on Ubuntu">
<img scr="images/img3.jpg" alt="terminal of vscode">
```
In python test code

```
driver.find_element(By.CSS_SELECTOR, "img[alt^='vscode']")
``` 
#### attribute ending with
here you need to use the $
```
<img scr="images/img1.jpg" alt="vscode running python script">
<img scr="images/img2.jpg" alt="usage of vscode on Ubuntu">
<img scr="images/img3.jpg" alt="terminal of vscode"> ✅
```
In python test code

```
driver.find_element(By.CSS_SELECTOR, "img[alt$='vscode']")
``` 
#### attribute containing
here you need to use the ~
```
<img scr="images/img1.jpg" alt="vscode running python script"> ✅
<img scr="images/img2.jpg" alt="usage of vscode on Ubuntu"> ✅
<img scr="images/img3.jpg" alt="terminal of vscode"> ✅
```
In python test code

```
driver.find_element(By.CSS_SELECTOR, "img[alt~='vscode']")
``` 
---
### CSS Selectors by Attribute of an element type
```
<input type="text" id="fistname" name="first_name" class="myForm">
```

In python test code

```
driver.find_element(By.CSS_SELECTOR, "input[name='first_name']")
``` 
---
### CSS Selectors by Id Attribute
In CSS, we can use # notation to select the id attribute of an element.

```
driver.find_element(By.CSS_SELECTOR, "input#fistname")
or
driver.find_element(By.CSS_SELECTOR, "#fistname")
```
---
### CSS Selectors by Class Attribute
The same principle can be used to locate elements by their class attribute.  
We use the . notation.   
```
driver.find_element(By.CSS_SELECTOR, "input.myForm")
or
driver.find_element(By.CSS_SELECTOR, ".myForm")
```   
**Extra info**: when the element has more than one class needed to access the element you needs to set the different classes
```
driver.find_element(By.CSS_SELECTOR, ".class1.class4")
```

