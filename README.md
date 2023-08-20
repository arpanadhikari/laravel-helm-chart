## Laravel Helm Chart

###

How to use this chart:

```bash
helm repo add laravel https://arpanadhikari.github.io/laravel-helm-chart/
helm install laravel laravel/laravel
```

By default, this chart will deploy a simple laravel container.

### Using your own image

Setting your own image for the Laravel application is as simple as setting the `image` parameter:

```bash
helm install --set image=your-own-image laravel .
```

There are a few pre-requisites for your image:

- The image must have a `/var/www/html` directory
- The laravel application must be in `/var/www/html
- The app should run on port `9000`
