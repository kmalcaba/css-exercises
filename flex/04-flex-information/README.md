# A very common website feature

The goal of this exercise is to recreate a section that is found on many informational websites.

For this one you will need to edit the HTML a little bit too. We can't be making things _too_ easy for you. You'll want to add containers around the various elements so that you can flex them. Good luck!

## Desired outcome

![desired outcome](./desired-outcome.png)

### Self Check

- All items are centered on the page (horizontally, not vertically).
- The title is centered on the page.
- There is 32px between the title and the 'items.'
- There is 52px between each item.
- The items are arranged horizontally on the page.
- The items are only 200px wide and the text wraps.
- The item text is centered.

### Solution

```css
.main, .fruit, .container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.main, .fruit {
  flex-direction: column;
}

.main {
  gap: 32px;
}

.container {
  gap: 52px;
}

.text {
  text-align: center;
}
```

```html
<div class="main">
    <div class="title">Information!</div>

    <div class="container">
        <div class="fruit">
            <img src="./images/barberry.png" alt="barberry">
            <div class="text">This is a type of plant. We love this one.</div>
        </div>

        <div class="fruit">
            <!-- content here -->
        </div>

        <div class="fruit">
            <!-- content here -->
        </div>

        <div class="fruit">
            <!-- content here -->
        </div>
    </div>

</div>
```

