[Laravel Sail](https://readouble.com/laravel/8.x/ja/sail.html) in [Visual Studio Code Remote Containers](https://code.visualstudio.com/docs/remote/containers).

# Usage

1. Install this tools.  
    - [Docker](https://www.docker.com/get-started)
    - [Visual Studio Code and extension](https://code.visualstudio.com/docs/remote/containers#_installation)

2. Clone this repository.  
```
git clone https://github.com/tsubakimoto/1009laravel
```

3. Install dependencies.  
```
cd 1009laravel
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v $(pwd):/var/www/html \
    -w /var/www/html \
    laravelsail/php81-composer:latest \
    composer install --ignore-platform-reqs
```

4. Open in Visual Studio Code.

5. Open the command palette (or type `F1`).

6. Select `Dev Containers: Open Folder in Container`.

7. Access to [http://localhost](http://localhost).
