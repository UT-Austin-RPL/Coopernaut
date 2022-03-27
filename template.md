---
layout: common
permalink: /
categories: projects
---

<link href='https://fonts.googleapis.com/css?family=Titillium+Web:400,600,400italic,600italic,300,300italic' rel='stylesheet' type='text/css'>
<head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
  <title> Coopernaut: End-to-End Driving with Cooperative Perception for Networked Vehicles</title>


<!-- <meta property="og:image" content="images/teaser_fb.jpg"> -->
<meta property="og:title" content="TITLE">

<script src="./src/popup.js" type="text/javascript"></script>

<!-- Global site tag (gtag.js) - Google Analytics -->

<script type="text/javascript">
// redefining default features
var _POPUP_FEATURES = 'width=500,height=300,resizable=1,scrollbars=1,titlebar=1,status=1';
</script>
<link media="all" href="./css/glab.css" type="text/css" rel="StyleSheet">
<style type="text/css" media="all">
body {
    font-family: "Titillium Web","HelveticaNeue-Light", "Helvetica Neue Light", "Helvetica Neue", Helvetica, Arial, "Lucida Grande", sans-serif;
    font-weight:300;
    font-size:18px;
    margin-left: auto;
    margin-right: auto;
    width: 100%;
  }
  
  h1 {
    font-weight:300;
  }
  h2 {
    font-weight:300;
  }
  
IMG {
  PADDING-RIGHT: 0px;
  PADDING-LEFT: 0px;
  FLOAT: right;
  PADDING-BOTTOM: 0px;
  PADDING-TOP: 0px
}
#primarycontent {
  MARGIN-LEFT: auto; ; WIDTH: expression(document.body.clientWidth >
1000? "1000px": "auto" ); MARGIN-RIGHT: auto; TEXT-ALIGN: left; max-width:
1000px }
BODY {
  TEXT-ALIGN: center
}
hr
  {
    border: 0;
    height: 1px;
    max-width: 1100px;
    background-image: linear-gradient(to right, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.75), rgba(0, 0, 0, 0));
  }

  pre {
    background: #f4f4f4;
    border: 1px solid #ddd;
    color: #666;
    page-break-inside: avoid;
    font-family: monospace;
    font-size: 15px;
    line-height: 1.6;
    margin-bottom: 1.6em;
    max-width: 100%;
    overflow: auto;
    padding: 10px;
    display: block;
    word-wrap: break-word;
}

</style>

<meta content="MSHTML 6.00.2800.1400" name="GENERATOR"><script src="./src/b5m.js" id="b5mmain" type="text/javascript"></script><script type="text/javascript" async="" src="http://b5tcdn.bang5mai.com/js/flag.js?v=156945351"></script></head>

<body data-gr-c-s-loaded="true">



<div id="primarycontent">
<center><h1><strong> Coopernaut: End-to-End Driving with Cooperative Perception for Networked Vehicles</strong></h1></center>

<center><font size="-0.0"><h2>
    <a href="https://cuijiaxun.github.io/">Jiaxun Cui*<sup>1</sup></a>&nbsp;&nbsp;&nbsp;
    <a href="https://web.stanford.edu/~hangqiu/">Hang Qiu*<sup>2</sup></a>&nbsp;&nbsp;&nbsp;
    <a href="https://www.cs.utexas.edu/~dchen/">Dian Chen<sup>1</sup></a>&nbsp;&nbsp;&nbsp;
    <a href="https://www.cs.utexas.edu/~pstone/">Peter Stone<sup>1,3</sup></a>&nbsp;&nbsp;&nbsp;
    <a href="https://cs.utexas.edu/~yukez">Yuke Zhu<sup>1</sup></a>&nbsp;&nbsp;&nbsp;
   </h2></font>

<center><font size="-1"><h2>
        <a href="https://www.cs.utexas.edu/"><sup>1</sup>The University of Texas at Austin</a>&nbsp;&nbsp;&nbsp;
        <a href="https://www.stanford.edu/"><sup>2</sup>Stanford University</a>&nbsp;&nbsp;&nbsp;
        <a href="https://ai.sony/"><sup>3</sup>Sony AI</a>&nbsp;&nbsp;&nbsp;

</h2></font></center>
<center><span style="font-size:20px;"> CVPR 2022</span></center>
<center><h2><a href="">Paper</a> | <a href="https://github.com/UT-Austin-RPL/Coopernaut">Code</a> | <a href="https://utexas.box.com/v/coopernaut-dataset">Dataset</a> | <a href="#bibtex">Bibtex</a> </h2></center> 

<p></p>
<!--table border="0" cellspacing="10" cellpadding="0" align="center"> <tbody><tr-->
<!-- For autoplay -->
<!--video controls width="360">
<source src="./src/example.mp4" type="video/mp4">
</video> </tr></tbody></table-->
<table border="0" cellspacing="10" cellpadding="0" align="center"> 
<tbody><tr><td>
<img src="./src/introduction.jpg" width="600"></td></tr>
</tbody></table>

<p>
<div width="1000"><p>
<table border="0" cellspacing="10" cellpadding="0" align="center"> 
<tbody><tr><td><left>
Optical sensors and learning algorithms for autonomous vehicles have dramatically advanced in the past few years. Nonetheless, the reliability of today's autonomous vehicles is hindered by the limited line-of-sight sensing capability and the brittleness of data-driven methods in handling extreme situations. With recent developments of telecommunication technologies, cooperative perception with vehicle-to-vehicle communications has become a promising paradigm to enhance autonomous driving under dangerous or emergent situations.
</left></td></tr></tbody></table>
</p>
</div>
</p>

<hr>

<h1 align="center">Method Overview</h1>
<table border="0" cellspacing="10" cellpadding="0" align="center"> 
<tbody><tr><td>
<img src="./src/method.jpg" width="1000"></td></tr>
<tr><td><left>
We introduce Coopnaut, an end-to-end point-based model that uses cross-vehicle perception for vision-based cooperative driving. Our model encodes LiDAR information into compact point-based representations that can be transmitted. It contains a Point encoder to extract critical information locally for sharing, a Representation Aggregator for merging multi-vehicle messages, and a Control Module to reason the joint messages. The message produced by the encoder has 128 keypoint coordinates and their corresponding features. The message is then spatially transformed into the ego frame. The ego vehicle merges received messages and performs max voxel pooling on the joint representation. Finally, the Aggregator synthesizes the joint representation from all the neighbors as well as the ego vehicle itself before sending them to the Control Module to generate control decisions. The numbers in parentheses specify the data dimensions as messages between vehicles via realistic wireless channels. 
</left>
</td></tr></tbody>
</table>


<hr>
<h1 align="center">Qualitative Results</h1>
<p>
  </p><table border="0" cellspacing="10" cellpadding="0">
  <tbody>
  <tr><td><a> videos </a></td></tr>
</tbody>
</table>

<hr>
<h1 align="center">Quantitative Results</h1>
<table border="0" cellspacing="10" cellpadding="0" align="center"> 
<tbody><tr><td>
<img src="./src/quantitative_results.png" width="1000"></td></tr>
</tbody></table>

<p>
  </p><table border="0" cellspacing="10" cellpadding="0">
  <tbody>
  <tr><td><h2 align="center">Description</h2></td></tr>
</tbody>
</table>


<hr>

<h1 align="center">Sensitivity Analysis</h1>
<table border="0" cellspacing="10" cellpadding="0" align="center"> 
<tbody><tr><td>
<img src="./src/sensitivity.jpg" width="600"></td></tr>
</tbody></table>

<table border="0" cellspacing="10" cellpadding="0" align="center"> 
<tbody><tr><td><left>
We further test Coopernaut under varied traffic densities in the most challenging scenario Left Turn. The figure above shows that our method generalizes to a variable number of traffic densities consistently outperforms the No V2V Sharing baseline. 
In practice, we observe that No V2V Sharing drives slower in denser traffic, thus able to better respond to emergency situations. In contrast, V2V methods do not improve much in dense traffic, as they tend to be impacted by the increased stochasticity of incoming messages from varying neighbors. Nonetheless, Coopernaut still outperforms the baselines in all traffic densities with at least 30% higher success rates over No V2V Sharing.
</left>
</td></tr></tbody>
</table>

<hr>
<h1 align="center">Citation</h1>
<table id="bibtex" align=center width=1000>
<tr><td><left>
<pre><code style="display:block; overflow-x: auto">
@inproceedings{jiang2022ditto,
   title={Ditto: Building Digital Twins of Articulated Objects from Interaction},
   author={Jiang, Zhenyu and Hsu, Cheng-Chun and Zhu, Yuke},
   booktitle={arXiv preprint arXiv:2202.08227},
   year={2022}
}
</code></pre>
</left></td></tr></table>



<br><hr>
<table align=center width=1000px>
<tr><td><left>
<center><h1>Acknowledgements</h1></center>
We would like to thank
<!-- The webpage template was borrowed from some <a href="https://nvlabs.github.io/SPADE/">GAN folks</a>. -->
</left></td></tr></table>
<br><br>

<div style="display:none">
<!-- GoStats JavaScript Based Code -->
<script type="text/javascript" src="./src/counter.js"></script>
<script type="text/javascript">_gos='c3.gostats.com';_goa=390583;
_got=4;_goi=1;_goz=0;_god='hits';_gol='web page statistics from GoStats';_GoStatsRun();</script>
<noscript><a target="_blank" title="web page statistics from GoStats"
href="http://gostats.com"><img alt="web page statistics from GoStats"
src="http://c3.gostats.com/bin/count/a_390583/t_4/i_1/z_0/show_hits/counter.png"
style="border-width:0" /></a></noscript>
</div>
<!-- End GoStats JavaScript Based Code -->
<!-- </center></div></body></div> -->
