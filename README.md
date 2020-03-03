<style TYPE="text/css">
code.has-jax {font: inherit; font-size: 100%; background: inherit; border: inherit;}
</style>
<script type="text/x-mathjax-config">
MathJax.Hub.Config({
    tex2jax: {
        inlineMath: [['$','$'], ['\\(','\\)']],
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'] // removed 'code' entry
    }
});
MathJax.Hub.Queue(function() {
    var all = MathJax.Hub.getAllJax(), i;
    for(i = 0; i < all.length; i += 1) {
        all[i].SourceElement().parentNode.className += ' has-jax';
    }
});
</script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=TeX-AMS_HTML-full"></script>

# Introduction to the bayesian approach in probability

This repository holds 3 notebooks that illustrates the bayesian approach and how it can be used in your project.  
The basics of the bayesian approach is that the parameters of a model are not point estimates but distributions that evolves with the observations. In most cases we can divide the approach into these steps:
- Define a model for your problem
- Put a prior distribution on your model parameters
- Apply Bayes rule iteratively, for each iteration take the posterior of the previous iteration as your new prior
The Bayes rule is:
$$P(A | B) = \frac{P(B | A) P(A)}{P(B)}$$
Its terms are:
- P(A) is the prior
- P(B | A) is the likelihood
- P(B) is the regularization parameter. It can be computed as a sum (discrete or continuous) of likelihoods for every value of A
- P(A|B) is the posterior
