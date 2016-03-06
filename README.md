# modernizr-override
A tool for providing a configurable override for Modernizr browser feature detection.

##What's it for?##

Modernizr is a great tool for browser feature detection, but there are times when it's useful to override Modernizr's detection and force the configuration of features that are available, both on the Javascript object and also the CSS marker classes. An example of this is when using Chrome Dev Tools to write fallback functionality for older mobile devices.

To help with this this is a simple modernizr-override helper to take a predefined Modernizr override and inject it on top of the detected features in Chrome. 

##Components##

- Manual opulation of the `window.ModernizrOverride` object.
- `modernizr-override.js`: Single self contained code file, or,
- `modernizr-override.min.js`: The above file manually uglified/minified using https://marijnhaverbeke.nl/uglifyjs

##To use##

- Download `modernizr-override.js` or `modernizr-override.min.js`
- Add a script tag directly after the script tag for `modernizr.js` or `modernizr-custom.js`.
- At a point earlier in the script sequence than the Modernizr scripts occur, set the value of window.ModernizrOverride.

For example you might have:

    <script type="text/javascript">
      window.ModernizrOverride = {flexbox: false, flexboxlegacy: true};
    </script>
    <script src="modernizr-custom.js" type="text/javascript"></script>
    <script src="modernizr-override.min.js" type="text/javascript"></script>



