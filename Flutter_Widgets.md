# Flutter Widgets

### Text: 

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

### Wrap:

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
            
