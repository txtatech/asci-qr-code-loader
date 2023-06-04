# ascii-qr-code-loader
A simple webpage that loads an ASCII QR-Code, extracts the JavaScript encoded in it and then executes the Javascript.

**Note 1:** 

This is very simillar to the [static](https://github.com/txtatech/static) project and is also used in the [forthttp](https://github.com/txtatech/forthttp) project.

**Note 2:** 

[Extra ASCII QR-Codes](https://github.com/txtatech/ascii-qr-code-loader/tree/main/Extra-ASCII-QR-Codes)
These QR-Codes contain the same code as those found in the [static](https://github.com/txtatech/static) project but are in ASCII form.
In theory they should accommodate loading the page (and its content) into the browser's memory, the cache, the DOM and as a binary string.
These files must be manually added to index.html to use them. Otherwise only the single QR-Code already found in index.html is loaded.

**Note 3:** 

The [ASCII-Base64-source.txt](https://github.com/txtatech/ascii-qr-code-loader/blob/main/ASCII-Base64-source.txt) is a copy of the Base64 encoded text used in making the ASCII QR-codes. This file is not required but was included as an example of how the JavaScript is formatted prior to being converted into ASCII QR-Codes.

**Note 4:** 

All JavaScript code loaded from the QR-Codes is stored in the DOM, in a Blob, in Memory and as a Binary String.

# ASCII Art Test (index.html)

This is a simple HTML page that contains an ASCII art QR-Code that is encoded as JavaScript code that gets executed. The page also includes some CSS styles to format the art and make it visible.

## HTML Structure

The HTML structure consists of a `head` and `body` section. In the `head`, there are two `style` blocks defining some CSS rules. The first `style` block sets the opacity of an element with the ID `ascii-art` to 0.5, making it partially transparent. The second `style` block sets the font family to monospace for all `pre` elements.

In the `body` section, there is a `pre` element with the ID `ascii-art` that contains the ASCII art. This element will be targeted by the JavaScript code.

## JavaScript Execution

The JavaScript code within the `pre` element will be executed when the page loads.

## Usage

To use this HTML page, simply open it in a web browser. The ASCII art will be displayed, and the JavaScript code from within the QR-Code will be executed.

If it does not load the code, refresh the page and check the Developer Tools Console for the output.

You should see that it starts (or attempts to start) a service-worker but fails because it is set to null. (Hence the 'Node' error)
Assigning the worker to null was done intentionally for security purposes.

**Note:**

I think the ASCII art can be made transparent (so it is not visible on the page) but I have not tinkered with that.

**Important Note:**

The spacing around the ASCII QR-Code is necessary for the reader to decode it properly. However you can add more ASCII QR-Codes directly below the first one as long as they all have the same afore-mentioned spacing.
