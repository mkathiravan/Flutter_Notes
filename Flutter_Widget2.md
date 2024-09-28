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
