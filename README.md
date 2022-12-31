## Features

a very simple flutter animated future builder which almost a complete replacement for FutureBuilder

## Usage

```dart

AnimatedFutureBuilder(
  future: getData(),
  builder: (BuildContext context,
    AsyncSnapshot<ProfileDataEntity?> snapshot) {
      if (snapshot.connectionState != ConnectionState.done) {
        return const Loading();
      }

      if (snapshot.hasError) {
        return const Text('error');
      }

      var profile = snapshot.data;
      if (profile == null) {
        return SizedBox();
      }
      return MyWidget(data: profile);
    }),
)

```
# animated_future_builder
