# jQuery FullScreen Plugin

A jQuery 1.7 plugin that wraps around the *Full Screen API* and works around various browser differences. Works in FF 10, Chrome and Safari.

## How to use

Include jquery.fullscreen.js in your page along with version 1.7 of the jQuery library. This gives you the `$('#elem').fullScreen()` method. You can optionally pass an object with properties:

<table>
	<tr>
		<th>Property</th>
		<th>Value</th>
		<th>Meaning</th>
	</tr>
    <tr>
        <td>background</td>
        <td>a color hash</td>
        <td>This is the color that will be used for the background.</td>
    </tr>
    <tr>
        <td>callback</td>
        <td>a function</td>
        <td>The callback function will be called on a full screen change event. It has one argument - a boolean indicating whether we are in full screen or not.</td>
    </tr>
</table>

After the plugin makes your element full screen, it will add the `.fullScreen` class on it, so you can easily style it.

## Example

```js
// The plugin sets the $.support.fullscreen flag:
if($.support.fullscreen){
	
	// ...
	// Show your full screen button here
	// ...
	
	$('#fullScreen').click(function(e){
	
		$('#content').fullScreen();
		
		// You can also pass a hash with properties:
		// $('#content').fullScreen({
		//	'background'	: '#111',
		//	'callback'		: function(isFullScreen){
		//		// ...
		//		// Do some cleaning up here
		//		// ...
		//	}
		// });
	});
}
```

You can then apply additional styles to your element:

```css

#content.fullScreen{
	/* Give the element a width and margin:0 auto; to center it. */
}

```

Take the opportunity to increase the font size, hide distractions and make for a better reading experience.

## Demo

Go to [Tutorialzine](http://tutorialzine.com/2011/12/countdown-jquery/) for a live demo.
