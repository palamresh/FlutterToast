# FlutterToast


import 'package:flutter/material.dart';
import 'package:fluttertoast/fluttertoast.dart';

void main() {
  runApp(const MaterialApp(home: MyHomePage()));
}

class MyHomePage extends StatefulWidget {
  const MyHomePage({super.key});

  @override
  State<MyHomePage> createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  ToastShow(text, Color) {
    Fluttertoast.showToast(
      msg: text,
      toastLength: Toast.LENGTH_SHORT,
      timeInSecForIosWeb: 1,
      gravity: ToastGravity.SNACKBAR,
      backgroundColor: Color,
      fontSize: 15.0,
      textColor: Colors.white,
    );
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
        appBar: AppBar(
          title: const Text('FormField Example'),
        ),
        body: Center(
          child: Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              ElevatedButton(
                onPressed: () {
                  ToastShow("My name is amresh", Colors.pink);
                },
                child: const Text('Show toast'),
              ),
              ElevatedButton(
                  onPressed: () {
                    ToastShow('File input', Colors.orange);
                  },
                  child: const Text('Show toast1'))
            ],
          ),
        ));
  }
}
