**21) Align**:

It is used to align its child widget within itself and optionally size itself based on the child's size.

Key Features:

Alignment: Positions its child within itself based on the alignment parameter.

Size Flexibility: Can optionally size itself to match the size of the child widget.

Parent Alignment: Can also be used to align itself within its parent widget.

Example 1: Creating a Align Widget

      Container(
         width: 200,
         height: 200,
         color: Colors.blue,
         child: Align(
      	alignment: Alignment.bottomRight,
      	child: Text(‘Aligned Text’),
      	),
      )

Example 2: Customizing Align Widget

        Container(
           width: 200,
           height: 200,
           color: Colors.blue,
           child: Align(
        	alignment: Alignment(0.5, -0.5),
        	child: Text(‘Custom Alignment’),
        	),
        )

Example 3: Handling Align Events

        Align(
           alignment: Alignment.center,
            child: GestureDetector(
        	onTap: () {
        	  // Add your onTap logic here
        	},
        	child: Container(
        	   color: Colors.red,
        	   width: 100,
        	   height: 100
        	)
        	)
        	)


**22) Padding**:

It is used to add padding space around its child widget.

Key Features:

Space Addition: Adds space around its child widget in all directions.

Flexible: Supports padding with EdgeInsets.symmetric, EdgeInsets.all, EdgeInsets.only etc

Visual Separation: Useful for visually separating widgets or providing spacing in UI layout.

Example 1: Creating a Padding Widget

            Padding(
                padding: EdgeInsets.all(16.0),
                child: Text(‘Padded Text’)
            )

Example 2: Customizing Padding Widget

            Padding(
               padding: EdgeInsets.symmetric(
            	vertical: 20,
            	horizontal: 10
              ),
             child: Text(‘Custom Padding’)
            )

Example 3: Handling Padding Events

            Padding(
               padding: EdgeInsets.all(16.0).
               child: GestureDetector(
            	onTap: () {
            		// Add your onTap logic here
            	},
            	child: Container(
            	  color: Colors.red,
            	  width: 100,
            	  height: 100
            	)
            	)
            )

**23) Center**:

It is used to center its child widget within itself or its parent widget.

Key Features:

Alignment: Center its child widget both horizontally and vertically.

Flexible: Can be used to center any type of widget.

Parent Alignment: Can also be used to center itself within its parent widget.

Example 1: Creating a Padding Widget

             Center(
                child: Text(‘Centered Text’,)
            )

Example 2: Handling Center Events

            Center(
                child: 	GetstureDetector(
                 onTap: () {
            	  // Add your onTap logic here
            	},
               child: Container(
            	color: Colors.blue,
            	width: 100,
            	height: 100
             ),
            ),
            )

**24) Expanded**:

It is used within a Row, Column, or Flex container to expand its child widget to fill the available space along the main axis.

Key features:

Flexibility: Expands its child widget to fill the available space along the main axis of the parent Row, Column or Flex.

Dynamic Sizing: Adjusts its size based on the available space and the sizes of the other widgets within the container.

Content Priority: Allows for prioritizing which widgets should expand if there's limited space.

Example 1: Creating an Expanded Widget

            Row(
              children: <Widget>[
                Expanded(
                     child: Text(‘Expanded Text’),
            	),
               // Add more widgets as needed
            ],
            )

Example 2: Handling Expanded Events

            Row(
               children: <Widget>[
            	Expanded(
            		child: GestureDetector(
            		onTap: () {
            			// Add your onTap logic here
            		},
            	   child: Container(
            		color: Colors.blue,
            		height: 100
            		),
            	),
            	),
            	// Add more widgets as needed
                ],
            )

**25) Flexible**:

It is used within a Row, Column, or Flex container to control how a child widget flexes along main axis.

Key Features:

Flexibility: Determines how much space a child widget occupies within its parent row, column or flex container.

Dynamic Sizing: Adjusts its size dynamically based on availbel space and flex factor.

Content priority: Allows for prioritizing which widgets should flex it there's limited space.

Example 1: Creating an Flexible Widget

            Row(
               children: <Widget>[
            	Flexible(
            	   child: Text(‘Flexible Text’)
            	),
            	// Add more widgets as needed
            	],
            )

Example 2: Handling Flexible Events

            Row(
               children: <Widget>[
            	Flexible(
            		child: GestureDetector(
            		onTap: () {
            			// Add your onTap logic here
            		},
            	   child: Container(
            		color: Colors.blue,
            		height: 100
            		),
            	),
            	),
            	// Add more widgets as needed
                ],
            )

**26) Spacer**:

It is used within a row or column to create flexible space between widgets, causing them to expand to fill the available space.

Key Features:

1. Flexibility: Automatically adjusts its size to fill the avialble space.

2. Dynamic Sizing: Expands or shrinks based on the space availble in its parent Row or Column.

3. Layout Control: Allows for easy creation of responsive layout with variable spacing.


Example 1: Using Spacer in a Row

            Row(
               children: <Widget>[
            	Flexible(
            	  child: Text(‘Flexible Text’)
            	)
            	]
            )

Example 2: Using Spacer in a Column

            Column(
               children: <Widget>[
            	Text(‘Top Text’),
            	Spacer(),
            	Text(‘Bottom Text’)
            	]
            )


**26) SizedBox**:

It is used to constrain the size of its child widget to a specific width and height.

Key Features:

Size Control: Sets the width and height of its child widget fo fixed dimensions.

Empty Spacer: Can also be used as an empty spacer to create space between widgets.

Precise Sizing: Provides precise control over the size of widgets within layouts.

Example 1: Creating SizedBox Widget

            SizedBox(
               width: 200,
               height: 100,
               child: Your Widget()
            )

Example 2: Using SizedBox as Spacer

            Column(
                children: <Widget>[
            	Container(
            	   color: Colors.green,
            	   width: 100,
            	   height: 100
            	),
                    SizedBox(height: 20),
            	Container(
            		color: Colors.red,
            		width: 100,
            		height: 100
            	),
            ],
            )
