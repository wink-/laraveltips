# Tired of that flash message lingering? Fade it out!

## jQuery
```javascript
<script>
$('div.alert').not('.alert-important').delay(3000).fadeOut(350);
</script>
```
## CSS
```css
<style type="text/css">
    
    div .alert-success {

    animation: flash-message 4s forwards;
    }

    @keyframes flash-message {
    0%   {opacity: 1;}
    100% {opacity: 0; display:none;}
    }
</style>
```
