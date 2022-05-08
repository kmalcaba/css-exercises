# A common 'modal' style
This one is another very common pattern on the web. The solution to this one is _simple_... but it might not be immediately obvious to you. You'll need to edit the HTML a bit to get everything where it needs to be.

### A hint
Depending on how you approach this one, you might need to revisit the `flex-shrink` property to keep a flex item from getting smashed.

## Desired outcome

![desired outcome](./desired-outcome.png)

### Self Check

- The blue icon is aligned to the left.
- There is equal space on either side of the icon (the gaps between the icon and the edge of the card, and the icon and the text, are the same).
- There is padding around the edge of the modal.
- The header, text, and buttons are aligned with each other.
- The header is bold and a slightly larger text-size than the text.
- The close button is vertically aligned with the header, and aligned in the top-right of the card.

### Solution

```css
.modal, .content, .title, .buttons {
  display: flex;
}

.modal {
  padding: 10px;
}

.title {
  justify-content: space-between;
  margin: 0 10px 0 10px;
  align-items: center;
}

.header {
  font-weight: 700;
  font-size: 110%;
}

.content {
  flex-direction: column;
  flex: 1;
  gap: 10px;
  margin: 10px 0;
}

.text{
  margin: 0 10px 5px 10px;
}

.buttons {
  gap: 10px;
}
```

```html
<div class="modal">
    <div class="icon">!</div>
    <div class="content">
        <div class="title">
            <div class="header">Are you sure you want to do that?</div>
            <div class="close-button">✖</div>
        </div>

        <div class="text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur excepturi id soluta, numquam minima rerum doloremque eveniet aspernatur beatae commodi. Cupiditate recusandae ad repellendus quidem consectetur sequi amet aspernatur cumque!</div>
        <div class="buttons">
            <button class="continue">Continue</button>
            <button class="cancel">Cancel</button>
        </div>
    </div>
</div>
```
