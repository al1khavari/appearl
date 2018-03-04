# Appearl
A super simple jQuery plugin checks if element is visible in page.

## Options
### `offset`
The appear check offset from top and bottom sides. To set top and bottom sides separately you can define an object containing `top` and `bottom`.

### `insetOffset`
Specifies the inside offset of element to check if it is visible. `insetOffset:'50%'` checks half of the element.

## Events
### `appear`
When the element comes inside the view.

### `disappear`
When the element leaves the view.

Both events pass data containing `from` value to specify direction of appearing or disappearing.

## Usage
```javascript
  $('.box').appearl({
      offset: {
        top: '20%',
        bottom: '40px'
      },
      insetOffset: '50%'
    }).on( 'appear disappear', function(event, data) {
      console.log(event.type, data.from);
    });
```