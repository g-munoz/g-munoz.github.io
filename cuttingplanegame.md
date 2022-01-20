---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: The Cutting Plane Game
permalink: /the-cutting-plane-game/
---

<h2><a href="http://www.columbia.edu/~gm2543/cpgame.html"><img class="alignnone size-full wp-image-315" src="../assets/cpgameco.png"></a></h2>
<h3>About</h3>
<p><strong>TL;DR:</strong> the cutting plane game was (slightly) updated and is hosted <a href="http://www.columbia.edu/~gm2543/cpgame.html" target="_blank" rel="noopener">HERE</a>.</p>
<p>This second version of the cutting plane game is a minor improvement from its previous version, which was released for the MIP Workshop 2019. Among other things, this new version contains a dedicated leaderboard for <a href="http://co-at-work.zib.de/">CO@Work 2020.</a> Participants should use their provided code to register their scores in the dedicated leaderboard. All scores (regardless of having the CO@Work code or not) will be registered in a global leaderboard.</p>
<p>Other changes with respect to the previous version are:</p>
<ul>
<li>The option of <span style="color: #ff0000;">restarting a level was removed</span>. There is still a bug resulting in a cut not created when it should, but the current version does not discount any budget in this case.</li>
<li>For this reason, <span style="color: #ff0000;">a new clean leaderboard was created</span>. Thanks to all that made it to the first leaderboard! You should confirm your skill now :)</li>
<li>A <span style="color: #ff0000;">new option of ending a level</span> was added to the pause menu. Use in case the level is stuck for some reason, or if you just don't like some polytope.</li>
<li>A new level was added, and an old annoying level was removed.</li>
<li>Minor bug-fixes.</li>
</ul>
<p>There are still some small bugs in the game, the most recurrent one being a cut not created when it should. Since the cut budget will not be decreased in this case, just try it again!</p>
<p>All feedback is greatly appreciated.</p>
<h3>Instructions</h3>
<p>The objective of the cutting plane game is simple: to get <strong><span style="color: #339966;">as close to the integer hull as possible.</span></strong></p>
<p dir="auto">In this version, there are 9 levels. If at any level you get the integer hull, <span style="color: #ff0000;"><strong>your total score will double!</strong></span> This is hard (and maybe impossible) on many levels though. Whenever you decide to end the game, you can upload your score to the online leaderboard.</p>
<p dir="auto">How do you get to the integer hull? Via cutting planes of course. There are 3 families of cuts: <strong><span style="color: #339966;">circle cuts</span></strong>, <strong><span style="color: #339966;">split cuts</span></strong> and<strong><span style="color: #339966;">&nbsp;Gomory cuts</span></strong>. In each level, you have a budget for each family, and you can continue cutting until your budget is zero or you have obtained the integer hull.</p>
<p><img src="../assets/level1-cpgame.jpg"></p>
<div dir="auto">&nbsp;</div>
<p dir="auto"><strong>You can also zoom in/out using the mouse wheel or trackpad.</strong></p>
<div dir="auto">&nbsp;</div>
<h4>Cut details</h4>
<p dir="auto"><strong><span style="text-decoration: underline;">Gomory cuts.</span></strong>&nbsp;When you select this cut family, the vertices of the polytope will be highlighted. If you click on one, and that vertex is not too close to being integer, a Gomory cut will be computed. The obvious question: which Gomory cut is computed? <span style="color: #ff0000;">The most violated one from the tableau.</span></p>
<p dir="auto"><span style="text-decoration: underline;"><strong>Circle cuts.</strong></span>&nbsp;When you select this family, you can click at any location on the screen and a circle of increasing radius will be created. The radius will increase until an integer point is hit by the circle. If any vertex of the polytope lies inside the circle, an intersection cut will be computed. The obvious question: is the cut computed with a conic relaxation? No, the actual convex hull of the polytope minus the circle is computed. In particular, two cuts from the same circle can be computed in some cases!</p>
<p dir="auto"><span style="text-decoration: underline;"><strong>Split cuts.</strong></span>&nbsp;These cuts work the same way as the circle cuts (since they are also intersection cuts). Note that you can select either vertical or horizontal split, but the <span style="color: #ff0000;">budget is shared</span> for both. With these, it's easier to see two cuts obtained from one set!</p>
<p><strong>Remark:</strong> for these last two families, it is <span style="color: #ff0000;">very important where you click</span> to create the circle or split. The lattice-free sets computed will not necessarily be maximal! In a situation like the following, for example, it might be hard to get a good split cut:</p>
<div dir="auto"><img src="../assets/level2-cpgame.jpg"></div>
<div dir="auto">&nbsp;</div>
<div dir="auto">So you might want to use a circle cut before the split ;)</div>
<div dir="auto">&nbsp;</div>
<div dir="auto">&nbsp;</div>
<p style="text-align: center;"><strong>I hope you enjoy the game!</strong></p>
