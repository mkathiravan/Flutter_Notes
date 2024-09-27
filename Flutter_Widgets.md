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

