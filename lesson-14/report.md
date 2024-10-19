# Отчет по практическому заданию

# Dart

Dart - это язык программирования, который используется для написания функционала, логики приложения, обработки данных и выполнения тех задач, которые выполняют ЯП.

## Пример скрипта

```dart
void main() {
  runApp(const MyApp());
}
// примеры части скрипта на Dart
void _incrementCounter() {
    setState(() {
      _counter++;
    });
```

# Flutter
Flutter - фреймворк, который скорее больше про верстку, стили, анимации, внешний вид приложения. Короче говоря он предоставляет необходимые инструменты для разработки пользовательского интерфейса (UI). Он использует `Dart`.

## Пример скрипта

```dart
class MyApp extends StatelessWidget {
  const MyApp({super.key});


  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepPurple),
        useMaterial3: true,
      ),
      home: const MyHomePage(title: 'Flutter Demo Home Page'),
    );
  }
}



class _MyHomePageState extends State<MyHomePage> {
// кроме этого вот
int _counter = 0;
  
  void _incrementCounter() {
    setState(() {
      _counter++;
    });
  }
// выделил комментами
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        backgroundColor: Theme.of(context).colorScheme.inversePrimary,
        title: Text(widget.title),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            const Text(
              'You have pushed the button this many times:',
            ),
            Text(
              '$_counter',
              style: Theme.of(context).textTheme.headlineMedium,
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: _incrementCounter,
        tooltip: 'Increment',
        child: const Icon(Icons.add),
      ), // This trailing comma makes auto-formatting nicer for build methods.
    );
  }
}

```
