# angular-tips-and-tricks
Tips and tricks for angular complex problems.

## Dynamic form elements with ng-repeat and ng-messages

```html
  <form name="form">
  <div class="asd" ng-repeat="item in [1,2,3,4,5]">
    <input ng-model="sub.name" name="subName@{{$index}}" class="form-control" placeholder="name" required maxlength="20" />
    <div class="field-error" ng-messages="form['subName' + $index].$error" ng-show="form['subName' + $index].$touched" role="alert">
        <div ng-message="required">Name is required.</div>
   </div>
  </div>
  <button type="submit" ng-disabled="form.$invalid" name="button">asdasd</button>
</form>
```

