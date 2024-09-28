# Flutter Widgets

### i) Container:

  It provides flexibility and control your UIs layout and apperance.

  Features:

   Padding: Space inside the container around its child widget.

   Margins: Space outside the container

   Borders: Lines surrouding the container.

   Background Color: Fill color for the container. 


           Container(
        	padding: EdgeInsets.all(16.0),
        	margin: EdgeInsets.all(16.0),
        	decoration: BoxDecoration(
        		color: Colors.blue,
        		border: Border.all(color: Colors.blue, width:2),
         		borderRadius: BorderRadius.circular(8.0),
        	),
        	child: Text(‘Hello, Container!’)
         )

### ii) Row :    

It is used to arrange child widgets in horizontal direction. Control alignment with mainAxisAlignment and crossAxisAlignment. Use Expand and Flexible for adaptive layouts.

Key features:

Alignment: Control how the children are aligned vertically.

Main Axis Alignment: Control how the children are spaced horizontally.

Children: Add multiple widgets inside the Row.

Example1:

                    Row(
             mainAxisAlignment: MainAxisAlignment.spaceEvenly,
             crossAxisAlignment: CrossAxisAlignment.Center,
              Children: <Widget>[
            	Icon(Icons.star),
            	Icon(Icons.star_border),
            	Icon(Icons.star_half),
            	],
              )
              

Example2:

              Row(
               children: <Widget>[
                 Expanded(
              	child: Text(‘This is a very long text should wrap or truncate’),
                ),
              Icon(Icons.more_horiz),
              ]
              )


### iii) Column:      

It is used to arrange child widgets in vertical direction.

 Key Features:

 Alignment: Control how the children are aligned horizontally.

 Main Axis Alignment: Control how the children are spaced vertically.

 Children: Add multiple widgets inside the column.

Example 1: 

           Column(
           mainAxisAlignment: MainAxisAlignment.spaceEvenly,
           crossAxisAlignment: CrossAxisAlignment.start,
            children: <Widget>[
          	Icon(Icons.star),
          	Icon(Icons.star_border),
          	Icon(Icons.star_half),
          	],
            )

Example 2: 

        Column(
           children : <Widget>[
        	Expanded(
        		child: Container(
        		  color: Colors.blue,
        		   child: Center(
        			child: Text( 			‘This container expands’,
        			‘to fill available space’
        			),
        		   ),
        		),
        	),
        	Icon(Icons.more_vert),
            ]
        )
      

### iv) Text: 

  It allows you to  display text various styles and alignments. 
  
  Use **Text** to display simple text of your flutter app. 

  Customize text apperarnce using text styles.

  Control text alignment within its container.

          Text(
             'Hello Flutter!',
             style: TextStyle(
               fontSize: 24.0,
               fontWeight: FontWeight.bold,
               color: Colors.blue
               )
          )

### v) Image:

 It is used to display images from different sources.

 Key Features:

  Image Sources: Load images from the asset bundle, network, memory or file.

  Image Formats: Supports various image formats such as JPEG, PNG, GIF, WebP, etc.

  Image Caching: Efficiently caches images to improve performance.

  
        Image.asset(‘assets/images/flutter_logo.png’)
        
        Image.network(‘https://example.com/image.jpg’)
        
        Image.asset(
           ‘assets/images/flutter_logo.png’,
           fit: BoxFit.cover,
           alignment: Alignment.center
        )

### vi) Icon:

It is used to display icon from various icon libraries.

Key Features:

Icon Libraries: Access icons from Material Icons, Cupertino Icons, and custom icon sets.

Icon Size and Color: Customize the size and color of icons to match your app's theme.

Icon Alignment: Align icon with their containers horizontally and vertically.

          Icon(
          	Icons.favorite,
          	size: 48.0,
          	color: Colors.red,
           )
          
          Icon(
          	MyCustomIcon.myIcon,
          	size: 48.0,
          	color: Colors.blue
          )

### vii) Raised Button:    

It is used to create buttons with a raised apperance.

Key Features:

Elevation: Adds a shadow to the button, giving it a raised apperance.

Tap Feedback: Provides visual feedback when the button is pressed.

Customization: Customize the button's color, text and shape.


        RaisedButton(
           onPressed: (){
        	// Add your onPressed logic here
        	},
            color: Colors.blue,
            shape: RoundedRectangleBorder(
        	borderRadius: BorderRadius.Circular(10.0),
        	),
             child: Text(‘Press Me’)	
          )


### viii) Flat Button:    

It is used to create text only button with no elevation.

Key Features:

Simplicity: Displays text without additional adornments like shadows.

Tap Feedback: Provides visual feedback when the button is pressed.

Cutomization: Customize the button's text, color, and onPressed behaviour.



              FlatButton(
             onPressed: (){
          	// Add your onPressed logic here
          	},
               child: Text(‘Press Me’, 
          	style: TextStyle(
          	  color: Colors.blue,
          	  fontSize: 18.0,
          	),
               ),
            )

### ix) FloatingActionButton:

It is used to create circular buttons that are typically placed in the bottom right corner of the screen.

Key Features:

 Prominence: Stands out from other UI elements making it ideal for primary actions.

 Elevation: Provides a shadow to give a button a floating apperance.

 Customization: Customize the button colors, icon and onPressed behaviour.


 
        FloatingActionButton(
            onPressed: (){
        	// Add your onPressed logic here
           },
          backgroundColor: Colors.blue,
          shape: RoundedRectangleBorder(
            borderRadius: BordeerRaidus.circular(10.0),
           ),
          child: Icon(Icons.add),
        )


### x) Scaffold:

It is a layout structure for the basic visual material design layout structure of the flutter app.

Key Features:

App Bar: Provides a top bar for displaying the title and actions.

Body: Defines the primary content of the screen.

Floating Action Button: Optional button that floats above the body content.

        Scaffold(
          appBar: AppBar(
             title: Text(‘My App’),
         ),
        body: Center(
           child: Text(‘Hello, Flutter!’),
        ),
        floatingActionButton: FloatingActionButton(
          onPressed() {
             // Add your onPressed logic here
         },
         child: Icon(Icons.add)
        ),
        )

### xi) AppBar:

 It is a material design widget that represent the top app bar in a Flutter app.

 Key Features:

 Title: Displays the title of the app.

 Actions: Optional action such as buttons, icons, or menus.

 Bottom: Additional widgets placed below the app bar, such as tabs.

 
          AppBar(
              title: Text(‘My App’),
              backgroundColor: Colors.blue,
              elevation: 0.0,
               leading:  IconButton(
          	icon: Icon(Icons.menu),
          	onPressed: () {
          		// Add your menu logic here
          	},
          	),
            )


### xii)BottomNavigationBar:

It is a material design widget that displays a horizontal row of tabs at the bottom of the screen.

Key Features:

Navigation: Allows users to switch between different screens or views within the app.

Icons: Each tab typically displays an icon and an optional label.

State Management: Automatically manages the selected tab state.

Example1:

            BottomNavigationBar(
            items: <BottomNavigationBarItem>[
        	BottomNavigationBarItem(
        	    icon: Icon(Icons.home),
        	    label: ‘Home’,
        	),
        	BottomNavigationBarItem(
        	    icon: Icon(Icons.search),
        	    label: ‘Search’,
        	), 	BottomNavigationBarItem(
        	    icon: Icon(Icons.person),
        	    label: ‘Profile’,
        	),
           ],
        )
        
Example2:
    
        BottomNavigationBar(
       items:  <BottomNavigationBarItem>[
    	// BottomNavigationBarItems..
      ],
      currentIndex: _selectedIndex,
      selectedItemColor: Colors.blue,
      onTap: _onItemTapped,
      type: BottomNavigationBarType.shifting
    )

### xiii)Drawer:

It is a material design widget that slides in from the edge of the screen to provide navigation options or other settings.

Key Features:

Navigation: Offers additional navigation options, settings or actions.

Edge Alignment: Typically aligned to the left or right edge of the screen.

Gesture Interaction: Can be opened and closed with a swipe gesture.

          Drawer(
             child : ListView(
          	padding: EdgeInsets.zero,
          	children: <Widget>[
          	  DrawerHeader(
          	   child: Text(‘Custom Header’),
          	   decoration: BoxDecoration(
          		color: Colors.green,
          	),
          	), 	ListTile(
          		title: Text(‘Custom Item 1’),
          		onTap: () {
          			// Add your onTap logic here
          	     },
          	),        ListTile(
          		title: Text(‘Custom Item 2 ’),
          		onTap: () {
          		 // Add your onTap logic here
          		},
          	),
                ],
             ),
          )

### iii) Wrap:

It is used to arrange its child widgets dynamically in a horizontal or vertical direction.

Customize the appearance and behaviour of the wrap using properties provided by Wrap.

Key Features: Dynamic arrangement, Flexible layout, Customizataion.

    Wrap(
     children: <Widget>[
       Container(
        width: 100,
          color: Colors.red,
       ),
        Container(
          width: 100,
         color: Colors.green,
        ),
       Container(
          width: 100,
         color: Colors.blue,
        ),
      ],
     )


### Table:

It is used to organize data in a grid of rows and columns.

Key Features: 

  Grid Layout: Organize data efficiently rows and columns.

  Flexible Sizing: Supports flexible sizing of rows and columns based on context.

  Customization: Allows customization of cells, borders, and more.


       
          body: Center(  
              child: Column(children: <Widget>[  
                Container(  
                  margin: EdgeInsets.all(20),  
                  child: Table(  
                    defaultColumnWidth: FixedColumnWidth(120.0),  
                    border: TableBorder.all(  
                        color: Colors.black,  
                        style: BorderStyle.solid,  
                        width: 2),  
                    children: [  
                      TableRow( children: [  
                        Column(children:[Text('Website', style: TextStyle(fontSize: 20.0))]),  
                        Column(children:[Text('Tutorial', style: TextStyle(fontSize: 20.0))]),  
                        Column(children:[Text('Review', style: TextStyle(fontSize: 20.0))]),  
                      ]),  
                      TableRow( children: [  
                        Column(children:[Text('Tutorial')]),  
                        Column(children:[Text('Flutter')]),  
                        Column(children:[Text('5*')]),  
                      ]),  
                      TableRow( children: [  
                        Column(children:[Text('Tutorial')]),  
                        Column(children:[Text('MySQL')]),  
                        Column(children:[Text('5*')]),  
                      ]),  
                    ],  
                  ),  
                ),  
              ])  
          )),  
        );  


### DataTable:

It is used to display tabular data in a series of rows and columns.

Key Features:

 Efficient Data Organization: Organizes data efficiently in rows and columns.

 Sortable Columns: Supports sorting columns by tapping on their headers.

 Customization: Allows customization of data cells, headers and more.


            DataTable(
            // datatable widget
              columns: [
                  // column to set the name
                  DataColumn(label: Text('Col1'),),
                  DataColumn(label: Text('Col2'),),
              ],
          
              rows: [
                  // row to set the values
                  DataRow(cells: [
                      DataCell(Text('ValCol1')),
                      DataCell(Text('ValCol2')),
                  ]),
              ],
          )
            
