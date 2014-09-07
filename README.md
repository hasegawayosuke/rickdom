# RickDOM - ricking DOM elements safety from string
	
----

RickDOM is a javascript library to build DOM elements from string using DOMParser API or createHTMLDocument API of modern browsers.

----
## Usage

    var rickdom = new RickDOM();
	var container = document.getElementById( "container" );
	var elements;
	var i;

	// read allowings property to show default rule 
	// div.textContent = JSON.stringify( rickdom.allowings, undefined, 2 );

	// write allowings property if you want to customize rule.
	// rickdom.allowings = { a : { href : { pattern : "^https?:\\/\\/", flag : "i" }, title : "" } };

	// build method returns array of HTMLElement.
	elements = rickdom.build( '<img src=# onerror=alert(1)><a href="http://example.jp/">example.jp</a><br><a href="javascript:alert(1)">javascript</a>' );
	for( i = 0; i < elements.length; i++ ){ 
	    container.appendChild( elements[ i ] );
	}

## Demo

Live demo is [here](http://utf-8.jp/public/rickdom/).

## License

See LICENSE file.





