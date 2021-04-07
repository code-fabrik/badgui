# Bad GUI

![bad guy icon](doc/badguy.png)

Bad GUI is a tiny GUI library for the web. It includes ready to use components
like prompts, alerts and sliders.

Bad gui does only generates the DOM structure for you but provides no styling
or design. You are responsible for the CSS.

## Usage

Embed badgui.js in your HTML file:

```html
<script src="https://example.com/badgui.js"></script>
```

### Components

#### Prompt

```js
const prompt = new badgui.prompt('Save', 'Please enter a name for the document', {
  inputs: [{
    label: 'Name', type: 'text', name: 'name'
  }],
  buttons: [{
    label: 'Cancel', action: function() {
      this.close();
    }
  }, {
    label: 'Save', action: function() {
      sendToServer(this.data());
      this.close();
    }
  }]
});

prompt.open();
```

