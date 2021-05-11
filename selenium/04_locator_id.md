# ID locator
IDs are the safest, fastest locator option and should always be your first choice. ID’s are supposed to be unique to each element.

## Example
In web code

```
<a id="change-password" class="btn" href="#">Forgotten Password</a>
```

In python test code

```
driver.find_element(By.ID, "change-password")
```