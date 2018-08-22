# JS Loader
### JS Loader is a lightweight jQuery plugin that helps you create an animated spinner with a fullscreen loading mask 
To use it you just have to include jQuery and a copy of JS Loader plugin in your head or footer:

```html
<script type="text/javascript" src="http://code.jquery.com/jquery-latest.js"></script>
<script src="../loader.js"></script>
```

#### Properies
| Attribute | Description | Example | Default Value |
| --- | --- | --- | --- |
| gifUrl | Url for a spinner gif image.| "./images/loader.gif" | NULL |
| bgRgab | Background color in Rgab format.| 'rgba(53, 53, 53, 0.8)' | 'rgba(53, 53, 53, 0.8)' |
| color | Loading Text color.| '#eaeaea' | 'White' |
| message | Loading Text | 'Please waite' | 'Loading...' |

#### Events
| Event | Description |
| --- | --- |
| onStartLoading | Fires when loading starts |
| onFinishLoading | Fires when loading starts |

#### Methds
| Methd | Description |
| --- | --- |
| show | To start showing loader |
| hide | To stop showing loader |
| setMessage | To set loading text |
| setHtmlMessage | To set loading text as html element

#### Basic Initialize

```html
$('#loader').loader();
```
#### Initialize with options

```html
$('#loader').loader({
    gifUrl: "./images/loader.gif",
    bgRgab:'rgba(53, 53, 53, 0.8)',
    color:'white'
});
```

#### Initialize with options and events

```html
$('#loader').loader({
    gifUrl: "./images/loader.gif",
    bgRgab:'rgba(53, 53, 53, 0.8)',
    color:'white',
    onStartLoading: function() {
        console.log("started loading");
    },
    onFinishLoading: function() {
        console.log("Finished loading");
    }
});
```

#### Method calls
```html
$('#loader').loader('setMessage', 'Please waite');
$('#loader').loader('setHtmlMessage', '<h1>Waiting..</h1>');
```

#### Show/Start loading (Method)
```html
$('#loader').loader('show');
```

#### Hide/Stopt loading (Method)
```html
$('#loader').loader('hide');
```
