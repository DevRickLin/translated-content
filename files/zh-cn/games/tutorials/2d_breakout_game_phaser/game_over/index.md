---
title: Game over
slug: Games/Tutorials/2D_breakout_game_Phaser/Game_over
tags:
  - 2D
  - Beginner
  - Canvas
  - Games
  - JavaScript
  - Phaser
  - Tutorial
  - game over
translation_of: Games/Tutorials/2D_breakout_game_Phaser/Game_over
---
<div>{{GamesSidebar}}</div>

<p>{{PreviousNext("Games/Workflows/2D_Breakout_game_Phaser/Player_paddle_and_controls", "Games/Workflows/2D_Breakout_game_Phaser/Build_the_brick_field")}}</p>

<div>
<p>这是<a href="/en-US/docs/Games/Workflows/2D_Breakout_game_Phaser">Gamedev Phaser 教程</a> 16 的<strong>第 8 步</strong>。在<a href="https://github.com/end3r/Gamedev-Phaser-Content-Kit/blob/gh-pages/demos/lesson08.html">Gamedev-Phaser-Content-Kit / demos / lesson08.html</a>完成本课后，您可以找到源代码。</p>
</div>

<p>为了使游戏更有趣，我们可以引入失去的能力 - 如果在到达屏幕底部边缘之前没有击球，那么这个游戏将会结束。</p>

<h2 id="如何输">如何输</h2>

<p>为了提供丢失的能力，我们将禁用球与屏幕底部的碰撞。在<code>create()</code>函数内添加下面的代码; 刚刚定义球的属性就好了：</p>

<pre class="brush: js">game.physics.arcade.checkCollision.down = false;
</pre>

<p>这将使三个墙壁（顶部，左侧和右侧）弹回球，但是第四个（底部）将消失，如果桨错过，则球从屏幕上脱落。我们需要一种方法来检测并相应地采取行动。在以前的新的下方添加以下行：</p>

<pre class="brush: js">ball.checkWorldBounds = true;
ball.events.onOutOfBounds.add(function(){
    alert('Game over!');
    location.reload();
}, this);
</pre>

<p>添加这些行将使得球检查世界（在我们的例子中是画布）边界并执行绑定到<code>onOutOfBounds</code>事件的函数。当您点击生成的警报时，页面将被重新加载，以便您可以再次播放。</p>

<h2 id="比较你的代码">比较你的代码</h2>

<p>您可以在下面的现场演示中查看本课程的完成代码，并使用它来更好地了解它的工作原理：</p>

<p>{{JSFiddleEmbed("https://jsfiddle.net/end3r/436bckb7/","","400")}}</p>

<h2 id="下一步">下一步</h2>

<p>现在的基本游戏就是让我们通过引入砖块来更有趣的是 - 现在是<a href="/en-US/docs/Games/Workflows/2D_Breakout_game_Phaser/Build_the_brick_field">建造砖块</a>的时候了。</p>

<p>{{PreviousNext("Games/Workflows/2D_Breakout_game_Phaser/Player_paddle_and_controls", "Games/Workflows/2D_Breakout_game_Phaser/Build_the_brick_field")}}</p>