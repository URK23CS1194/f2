
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        appBar: AppBar(
          title: Text("Restaurant Menu"),
          backgroundColor: Colors.orange,
        ),

        body: LayoutBuilder(
          builder: (context, constraints) {

            if (constraints.maxWidth < 600) {

              // Mobile Layout
              return Column(
                children: [

                  Card(
                    child: ListTile(
                      leading: Icon(Icons.fastfood),
                      title: Text("Burger"),
                      subtitle: Text("Rs.120"),
                    ),
                  ),

                  Card(
                    child: ListTile(
                      leading: Icon(Icons.local_pizza),
                      title: Text("Pizza"),
                      subtitle: Text("Rs.200"),
                    ),
                  ),

                  Card(
                    child: ListTile(
                      leading: Icon(Icons.lunch_dining),
                      title: Text("Sandwich"),
                      subtitle: Text("Rs.80"),
                    ),
                  ),

                ],
              );

            } else {

              // Desktop Layout
              return Row(
                children: [

                  Expanded(
                    child: Card(
                      child: ListTile(
                        leading: Icon(Icons.fastfood),
                        title: Text("Burger"),
                        subtitle: Text("Rs.120"),
                      ),
                    ),
                  ),

                  Expanded(
                    child: Card(
                      child: ListTile(
                        leading: Icon(Icons.local_pizza),
                        title: Text("Pizza"),
                        subtitle: Text("Rs.200"),
                      ),
                    ),
                  ),

                  Expanded(
                    child: Card(
                      child: ListTile(
                        leading: Icon(Icons.lunch_dining),
                        title: Text("Sandwich"),
                        subtitle: Text("Rs.80"),
                      ),
                    ),
                  ),

                ],
              );

            }
          },
        ),
      ),
    );
  }
}

