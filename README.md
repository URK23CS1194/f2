
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text("Restaurant Menu"),
        ),

        body: LayoutBuilder(
          builder: (context, constraints) {

            if (constraints.maxWidth < 600) {
              return Column(
                children: [
                  Card(
                    child: ListTile(
                      title: Text("Burger"),
                      subtitle: Text("Rs.120"),
                    ),
                  ),

                  Card(
                    child: ListTile(
                      title: Text("Pizza"),
                      subtitle: Text("Rs.200"),
                    ),
                  ),

                  Card(
                    child: ListTile(
                      title: Text("Sandwich"),
                      subtitle: Text("Rs.80"),
                    ),
                  ),
                ],
              );
            }

            else {
              return Row(
                children: [
                  Expanded(
                    child: Card(
                      child: ListTile(
                        title: Text("Burger"),
                        subtitle: Text("Rs.120"),
                      ),
                    ),
                  ),

                  Expanded(
                    child: Card(
                      child: ListTile(
                        title: Text("Pizza"),
                        subtitle: Text("Rs.200"),
                      ),
                    ),
                  ),

                  Expanded(
                    child: Card(
                      child: ListTile(
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
