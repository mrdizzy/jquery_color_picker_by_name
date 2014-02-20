<html>
<body>
<p>If you want an absolutely positioned element to be positioned <i>relative</i> to its <i>parent</i>, then the <i>parent</i> needs to have <code>position: relative</code> set in its css. More information: 
<ul>
<li>
<a href="http://css-tricks.com/absolute-positioning-inside-relative-positioning/">http://css-tricks.com/absolute-positioning-inside-relative-positioning</a></li>
<li><a href="http://www.barelyfitz.com/screencast/html-training/css/positioning/">http://www.barelyfitz.com/screencast/html-training/css/positioning/</li>
<li><a href="http://www.w3.org/TR/CSS21/visuren.html#comp-abspos">http://www.w3.org/TR/CSS21/visuren.html#comp-abspos</a></li>
</ul>

<p>The abs-positioned elements are positioning themselves against the first ancestor not static postitioned, and there is none here, so they position against html (this can be seen by adding margin-top to body, and the Back-Home image is not moved).</p>
<p>
The containing block for a positioned box is established by the nearest positioned ancestor (or, if none exists, the initial containing block, as in our example).

</p>
<div style="width:50%;border:1px solid blue;height:50px;">This is a container without <code>position: relative</code>
  <div style="position:absolute;width:60%;height:35px;border:1px solid green;">This is an absolutely positioned element inside the container. Its width is relative to the <i>window</i> rather than the parent container element.</div>
</div>


<div style="padding:50px;"></div>
<div style="width:50%;border:1px solid blue;height:50px;">This is a container without <code>position: relative</code>
  <div style="position:absolute;top:50px;right:50px;width:60%;height:35px;border:1px solid green;">This is an absolutely positioned element inside the container. Its width is relative to the <i>window</i> rather than the parent container element.</div>
</div>


<div style="padding:50px;"></div>
<div style="position:relative;width:50%;border:1px solid blue;height:50px;">This is a container without <code>position: relative</code>
  <div style="position:absolute;width:60%;height:35px;border:1px solid green;">This is an absolutely positioned element inside the container. Its width is relative to the <i>parent</i> rather than the window.</div>
</div>
</body>

</html>

