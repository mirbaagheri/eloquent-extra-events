# eloquent-extra-events

>Note: This package is compatible with Laravel 5.5.X only.

Installation
------------

**Install:**

`composer require mirbaagheri/eloquent-extra-events`


Usage
------
**Load package:**

You just have to load `ExtraEventsTrait` in your `Eloquent Model`:

`use MostafaMiri65\EloquentExtraEvents\ExtraEventsTrait;`


**Events:**
  * eloquent.syncing
  * eloquent.synced
  * eloquent.attaching
  * eloquent.attached
  * eloquent.detaching
  * eloquent.detached

**Listeners:**

Listen to above events in: `App\Providers\EventServiceProvider`:

Global listener:
```
Event::listen('eloquent.syncing*', function ($eventName, array $eventData) {

    //Do something ...

});

```
Specific Listener:
````
Event::listen("eloquent.attaching: App\YourCustom\EloquentCustom*", function ($eventName, array $eventData) {

    //Do something ...
            
        });
````

LICENSE
----------
This package is released under MIT license.

