What if you have a collection of carbon objections, but you need to feed your view an array of dates? Lets assume you have a temperature data logger that records a temperature every minute and you want to plot that temperature vs the timestamp.
```
Temperature::where('record_id', 1)->orderBy('created_at', 'desc')->take(1440)->get();
```
This will return a collection of the past day's (1440 mins) times as carbon objects. ChartJS wants the date as a DateTimeString, not a carbon object. We have to convert these to an array via the following:
```
array_column(Temperature::where('record_id', 1)->orderBy('created_at', 'desc')->take(1440)->get()->toArray(), 'created_at');
```
