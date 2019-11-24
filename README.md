laravel-admin-tagsinput
======
Интегральная `bootstrap-tagsinput` из `laravel-admin` `Form` распространение

Предоставление
-
![result.png](https://github.com/namet117/images/raw/master/laravel-admin-tags/result.png)

Окружающая среда
-
* php `>= 7`
* laravel-admin `~1.6`

Монтаж
-
1.Установка с помощью composer
```shell
composer require fotobank/laravel-admin-tagsinput -vvv
```
2.Публикация статических ресурсов
```shell
php artisan vendor:publish --tag=laravel-admin-tagsinput
```

3.Использование в контроллере `tagsinput` метод
```php
// app/Admin/Controllers/GoodsController

protected function form()
{
    $form = new Form(new GoodsCate);

    $form->text('name', 'Название');
    $form->switch('nullable', 'Switch')->default(1);
    $form->tagsinput('values', 'Дополнительное значение');
    return $form;
}
```

LICENSE
-
MIT


