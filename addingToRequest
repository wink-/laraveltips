## Artificially adding values to the Request array

All credit to http://laraveldaily.com/how-to-artificially-add-values-to-request-array/ and its comments

```
function store(Request $request) 
{
  // some additional logic or checking
  $plan = 123; // some logic to decide user's plan
  $request->request->add(['plan' => $plan]);
  //or
  User::create($request->all() + ['plan' => $plan]);
  //or
  User::create(array_merge($request->all(), ['plan' => $plan]));
  
  
  //Add values to the Request array:
  array_add($request->all(), 'user_id', $user->id);

  //Remove values from the Request array:
  array_except($request->all(), ['screenshot', 'webcam']);
  
  //or
  Request::merge(array(‘user_id’ => Auth::id()));
  
  //or
  Request::merge(array(‘user_id’ => Auth::id()));
  
  User::create($request->all());
}
```
