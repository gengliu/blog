# 一些有用的css样式总结

## 自定义radio

### code

```html
<div class="radio-beauty-container">
    <label>
        <span class="radio-name">前端工程师</span>
        <input type="radio" name="radioName" id="radioName1" hidden/>
        <label for="radioName1" class="radio-beauty"></label>
    </label>
    <label>
        <span class="radio-name">后端工程师</span>
        <input type="radio" name="radioName" id="radioName2" hidden/>
        <label for="radioName2" class="radio-beauty"></label>
    </label>
    <label>
        <span class="radio-name">全栈工程师</span>
        <input type="radio" name="radioName" id="radioName3" hidden/>
        <label for="radioName3" class="radio-beauty"></label>
    </label>
</div>
```

```scss
.radio-beauty-container {
  font-size: 0;
  $bgc: green;
  %common {
    padding: 2px;
    background-color: $bgc;
    background-clip: content-box;
  }
  .radio-name {
    vertical-align: middle;
    font-size: 16px;
  }
  .radio-beauty {
    width: 18px;
    height: 18px;
    box-sizing: border-box;
    display: inline-block;
    border: 1px solid $bgc;
    vertical-align: middle;
    margin: 0 15px 0 3px;
    border-radius: 50%;
    &:hover {
      box-shadow: 0 0 7px $bgc;
      @extend %common;
    }
  }
  input[type="radio"]:checked + .radio-beauty {
    @extend %common;
  }
}
```

### result

![result](../assets/radio-self.png)



