# PAG JS - Prismatic Animated Gallery

**Script Name:** 	PAG JS   
**Library URL:**	https://www.stefanofattori.it/pag-js/    
**Author:**     	Stefano Fattori   
**Author Website:**	https://www.stefanofattori.it   
**Description:** PAG JS is an animated and filterable vanilla Javascript library gallery with pagination, beautiful animations and customisable parameters.    
**Browser compatibility:** This script uses Animate() Javascript function. Check you browser compatibility at https://developer.mozilla.org/en-US/docs/Web/API/Element/animate    
**License:**    	Commercial    
**License URL:**	https://www.stefanofattori.it/pag-js/license/


## Description

PAG JS is an animated and filterable gallery with pagination, beautiful animations and customisable parameters.  
This script use modern Vanilla Javascript and it has no dependencies on external libraries.    

The script file size ~ 15 KB

## Installation and Usage 

1. Download and import the script into your HTML file simply using:  
```
 <script src="pag-js.min.js"></script>   
```
OR using CDN:
```     
 <script src="https://cdn.jsdelivr.net/gh/stefanofattori/pag-js@v1.1/dist/pag-js.min.js"></script> 
```

2. Initialises a constant variable with the parameters:  
```
	const options = {
                containerClass: '.gallery',          // gallery container - Default: .pag-gallery
                itemContainerClass: '.item',         // gallery item - Default: .item
                paginationClass: '.pagination',      // pagination buttons - Default: .pagination
                filtersClass: '.filters',            // filter buttons - Default: .filters
                aspectRatio: '16 / 9',               // images aspect ratio - Default: 3 / 2
                gap: 10,                             // supports only px - Default: 10
                itemsPerPage: 12,                    // number of items per page to show ( 0 -> Disable Pagination ) - Default: 0
                columns: {                           // colums number of layout (responsive)
                    HD: 4,                           // Desktop HD > 1200px - Default: 4/3/2/1
                    DESKTOP: 3,                      // Desktop    > 1024px  
                    TABLET: 2,                       // Tablet     > 768px
                    SMARTPHONE: 1                    // Smartphone < 768px  
                },
                objectFit: 'cover',                  // Items Image CSS behavior ( contain|cover|fill|scale-down|none ) - Default: cover
                animation: 'slide',                  // Animation type (none|fade|zoom|slide|smart) - Default: smart
                animationDuration: 0.4,              // Animation duration (s) - Default: 0.5
                easing: 'linear',                    /* Animation easing type. All CSS easing ( linear|ease|ease-in|ease-out|ease-in-out|step-start|step-end|steps(int,start|end)|cubic-bezier(n,n,n,n)|initial|inherit )
                                                        Default: linear
                                                        example - simulate bounce1: cubic-bezier(0.68, -0.55, 0.27, 1.55) 
                                                        example - simulate bounce2: cubic-bezier(0.34, 1.56, 0.64, 1) */
                animationAsync: false,               /* FALSE -> the display animations will start after the hiding animations have finished                
                                                        TRUE -> the display animations will start immediately together with the hiding animations 
                                                        Default: true */
                defaultFilter: 'all'                 // Default filter - Default: all

            };
```

3. Initialises the class:  
``` 
	const gallery = new PagJS(options); 
``` 

4. Use ` data-categories="1" ` to set the membership of the item element to the respective filter.    
   Use ` data-filter="all" ` to set to set the filter to be activated on the button	

5. HTML structure could be like this example: 
``` 
    <div class="filters">
        <button data-filter="all">ALL</button>
        <button data-filter="1">FILTER 1</button>
        <button data-filter="2">FILTER 2</button>
        <button data-filter="3">FILTER 3</button>
    </div>

	<div class="pag-gallery">
		<div class="item" data-categories="1">
			<figure>
				<img src="" alt="Image 1">
				<figcaption>Image 1</figcaption>
			</figure>
		</div>

		<div class="item" data-categories="2">
			<figure>
				<img src="" alt="Image 2">
				<figcaption>Image 2</figcaption>
			</figure>
		</div>

		<div class="item" data-categories="1,2">
			<figure>
				<img src="" alt="Image 3">
				<figcaption>Image 3</figcaption>
			</figure>
		</div>

		<div class="item" data-categories="3">
			<figure>
				<img src="" alt="Image 4">
				<figcaption>Image 4</figcaption>
			</figure>
		</div>
	</div>

	<div class="pagination"></div>
```

## Browser support
All modern browsers.   
Old IE is not supported.

## Donate
Did you enjoy PAG JS? PAG JS is entirely created and supported by me, it's sold at a very cheap price, if you like the library and would like to make a further contribution to the project, feel free to donate:       

https://paypal.me/stefanofattori89


## Privacy 
PAG JS  doesn't uses LocalStorage to save the setting.  
No data is saved in the database or transferred.  


## === Changelog ===

#### = 1.2 =
* [FIX] - Added error handling on non-existent html elements

#### = 1.1 =
* [NEW] - Added add and remove active class to filter buttons elements
* [NEW] - Set a transition attribute when the container changes its height

#### = 1.0 =
* [NEW] - First version of the script written  


## License
PAG JS is licensed under a Commercial License. Enjoy! 


*Everything else used in this script has been created by me (Stefano Fattori), especially for the PAG JS script and is distributed under Commercial license.*  
