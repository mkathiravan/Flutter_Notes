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
