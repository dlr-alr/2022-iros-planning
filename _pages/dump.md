
|                                     Noise                                     |                                          Occupancy Grid                                           |                                                   A                                                   |
|:-----------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------:|
| ![BPS - Build](../assets/imgs/bps/bps_build.gif){:.this style="width: 400px"} | ![BPS - Distances Lines](../assets/imgs/bps/bps_distances_lines.gif){:.this style="width: 400px"} | ![BPS - Distances Circles](../assets/imgs/bps/bps_distances_circles.gif){:.this style="width: 400px"} |


custom head
<link rel="icon" type="image/svg+xml" href="{{ '/assets/favicon/favicon.svg' | relative_url }}">
<link rel="icon" type="image/png" href="/assets/favicon/favicon.png">


 <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
      tex2jax: {
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
        inlineMath: [['$','$']]
      }
    });
 </script>
  <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

<!-- Mathjax Support -->
<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>



Those examples show the problem with inconsistent labels.
While more computational resources can solve those problems it is more efficient to use the help of the network as guidance.
Using the prediction of the network as indicator is also more general, then applying some custom heuristics to identify potential outliers.

![wrong labels](../assets/imgs/methods/wrong_labels.png){:.this 
style="width: 800px; 
display: block;
margin-left: auto;
margin-right: auto"}