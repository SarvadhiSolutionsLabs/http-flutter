# http-flutter
A composable, Future-based library for making HTTP requests. This library use http package


## Features

- Contain all HTTP requests in sepearte file and return one common class to hadle HTTP request like a pro.
- Check for internet connection before calling any API
- Return common class RequestResponse for all types of HTTP request
- Can make multi-part request

## Installation

Install the dependencies in pubspecs.yaml file

```sh
http_kit:
  git:
    url: https://github.com/SarvadhiSolutionsLabs/http-flutter.git
```

## Using the library

```sh
Future _getPost() async {
    const String url = 'https://jsonplaceholder.typicode.com/posts';
    final RequestResponse _response = await HttpKit.get(url);
    print(_response);
    _posts = PostModel.fromJson(_response.data);
    print(_posts);
}
```
