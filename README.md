# RouletteGame
Easy constructor game roulette

##Getting started
1. Include jQuery
2. Include RouletteGame files (js and css)
3. Create istance RouletteGame with your options after document ready
```html
<link rel="stylesheet" href="src/RouletteGame.css">
<script src="src/jquery-1.12.0.min.js"></script>
<script src="src/RouletteGame.js"></script>
<script>
    $(document).ready(function() {
      var instance = new RouletteGame({
         insert: $('.js-game-container'),
         duration: 13,
         callback: function (winner) {
           console.log('this winner - ' + winner)
         }
      });
      instance.push({
        name: 'Michael',
        procent: 50,
        bet: 100,
        html: '<div class="player-item table"><div class="player-text table-cell">Michael</div></div>'
      });
      instance.render().start();
    });
</script>
```

##Options
<code>cell</code> - number of cells
<code>stopCell</code> - 
<code>visibleCell</code> - visible cells
<code>duration</code> - duration run in seconds
<code>easing</code> - animate easings transition
<code>wrapperClass</code> - add custom class to container
<code>insert</code> - where to insert (jQuery object)
<code>callback</code> - callback function after end game


##Public methods
<code>instance.render()</code> - render HTML current game
<code>instance.start()</code> - start current game
<code>instance.push({} || [{}, {}])</code> - push items in storage
<code>instance.remove(index)</code> - remove item from storage
<code>instance.getBank()</code> - get current bank
<code>instance.getStorage()</code> - get storage bank
<code>instance.getWinner()</code> - get last winner
<code>instance.clearStorage()</code> - clear storage
<code>instance.clearBank()</code> - clear bank


##Browser Support
All modern browsers and IE9+
roulettegame

##Example
See detail example - <a href="http://m-ulyanov.github.io/roulettegame/">RouletteGame</a>