# Name locator
Name locator comes after ID. If any web element has not ID attribute, we can use name attribute if available. Name cannot be unique all the times. If there are multiple names, Selenium will always perform action on the first matching element.

## Example
In web code

```
<button type="button" name="cake" value="Strawberry">Strawberry</button>
```

In python test code

```
driver.find_element(By.NAME, "cake")
```