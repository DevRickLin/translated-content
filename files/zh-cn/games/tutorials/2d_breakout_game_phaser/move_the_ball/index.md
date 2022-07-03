---
title: Move the ball
slug: Games/Tutorials/2D_breakout_game_Phaser/Move_the_ball
tags:
  - 2D
  - Beginner
  - Canvas
  - Games
  - JavaScript
  - Phaser
  - Tutorial
  - moving
translation_of: Games/Tutorials/2D_breakout_game_Phaser/Move_the_ball
---
<div>{{GamesSidebar}}</div>

<p>{{PreviousNext("Games/Workflows/2D_Breakout_game_Phaser/Load_the_assets_and_print_them_on_screen", "Games/Workflows/2D_Breakout_game_Phaser/Physics")}}</p>

<div>
<p>这是<a href="/en-US/docs/Games/Workflows/2D_Breakout_game_Phaser">Gamedev Phaser 教程</a> 16 的<strong>第 4 步</strong>。在<a href="https://github.com/end3r/Gamedev-Phaser-Content-Kit/blob/gh-pages/demos/lesson04.html">Gamedev-Phaser-Content-Kit / demos / lesson04.html</a>完成本课后，您可以找到源代码。</p>
</div>

<p>我们在屏幕上打印了我们的蓝色球，但它什么都不做，这样做会很酷。本文介绍如何做到这一点。</p>

<h2 id="在每个框架上更新球的位置">在每个框架上更新球的位置</h2>

<p>记住<code>update()</code>功能及其定义？其中的代码在每个框架上执行，所以它是一个完美的地方，将代码更新球的位置在屏幕上。在里面添加以下新行代码<code>update()</code>，如下所示：</p>

<pre class="brush: js">function update() {
    ball.x += 1;
    ball.y += 1;
}
</pre>

<p>上面的代码在每个框架上为表示画布上的球坐标的属性<code>x</code>和<code>y</code>属性添加了一个。重新加载 index.html，你应该看到球在屏幕上滚动。</p>

<h2 id="比较你的代码">比较你的代码</h2>

<p>您可以在下面的现场演示中查看本课程的完成代码，并使用它来更好地了解它的工作原理：</p>

<p>{{JSFiddleEmbed("https://jsfiddle.net/end3r/g1cfp0vv/","","400")}}</p>

<h2 id="下一步">下一步</h2>

<p>下一步是添加一些基本的碰撞检测，所以我们的球可以从墙壁反弹。这将需要几行代码 - 一个比我们迄今为止看到的更复杂的步骤，特别是如果我们也想添加桨和砖碰撞 - 但是幸运的是 Phaser 使我们比我们想要使用纯粹的方法更容易做到这一点 JavaScript 的。</p>

<p>无论如何，在我们做所有的事情之前，我们将首先介绍 Phaser 的<a href="/en-US/docs/Games/Workflows/2D_Breakout_game_Phaser/Physics">物理</a>引擎，并做一些设置工作。</p>

<p>{{PreviousNext("Games/Workflows/2D_Breakout_game_Phaser/Load_the_assets_and_print_them_on_screen", "Games/Workflows/2D_Breakout_game_Phaser/Physics")}}</p>