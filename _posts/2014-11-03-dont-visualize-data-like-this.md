---
title: "Don't Visualize Data Like This"
author: steve
layout: post
permalink: /blog/2014/11/dont-visualize-data-like-this/
categories:
  - Uncategorized
---

Facebook's Data Science blog should not visualize data like this.

<!--more-->

Facebook's Data Science blog published some observations of Facebook users in light of the upcoming Midterm elections. The premise was simple. Politics at the mass-level and institution-level seem as polarized as ever. With the midterm elections approaching, what can we say about pop culture differences between Facebook users who self-identify as Republicans and Facebook users who self-identify as Democrats?

[The ensuing post][1] from Facebook&#8217;s Data Science blog generated a fair bit of interest, especially with data visualizations like this.

{% include image.html url="/images/facebook-data-science-music-preferences.png" caption="Music preferences of Facebook users, color-coded between Republicans (red) and Democrats (blue)." width=720 align="center" %}

The graph (among others listing where Facebook users visit, what TV shows they watch, and what authors they read) caught the attention of general interest websites. This led to some headlines like [&#8220;Why Do Republicans Hate the Beatles?&#8221;][2] to accentuate what this graph purports to tell an audience.<sup><a href="#footnote_0_97" id="identifier_0_97" class="footnote-link footnote-identifier-link" title="From my perspective, the more pressing question would be why doesn&rsquo;t everyone love Mary J. Blige. She&rsquo;s awesome, but alas.">1</a></sup>

The problems with these graphs are multiple. If this were for a class I would teach on data visualization, it might not get a passing grade.

By using a format akin to a [scatterplot][3], the graph purports to a show a bivariate relationship. Absent any additional information, it&#8217;s suggests a bivariate relationship between partisanship (on the *x-*axis) and liking certain musical artists (on the *y-*axis). As partisanship (on a Democrat-to-Republican scale) increases, a Facebook user is more likely to like Ted Nugent&#8217;s Facebook page relative to someone who scores lows on partisanship (i.e. someone who self-identifies as a Democrat). This would conform well with how Mother Jones interpreted it.

However, that&#8217;s not what the graph shows, nor is the Facebook user even the unit of analysis. Facebook&#8217;s Data Science blog needed this preface to the graphs provided on its blog.

> <span style="color: #141823;">Note: in all of the figures below, the more a page is disproportionately liked by fans of Republican candidates, the farther right the page name appears (precisely indicated by the darker line in the middle). Conversely, the more a page is disproportionately liked by fans of Democratic candidates, the farther left the page name appears. The font size of the name is proportional to the total number of people from the US who liked that page.</span>

A preface to interpreting graphs this long-winded already jeopardizes the entire endeavor. Having to follow it with [a clarification like this in the comment section][4] means the plot is lost.

> <span style="color: #141823;">The y axis is basically meaningless, just giving room for the name so they can appear at the right place on the x-axis, which is the difference in proportion of R or D fans who liked the page. The x-axis is scaled so that the plot is centered around zero and the largest absolute value is at the edge of the plot.</span>

A two-dimensional graph should not have a *y*-axis that is &#8220;basically meaningless&#8221;. Bad Facebook Data Science blog. Bad.

While the graph would lend itself to an easy interpretation of a comparison of culture tastes of Republican users and Democrat users, this is not at all what the graph communicates. The unit of the analysis is the Facebook *page*, not the Facebook user. Facebook&#8217;s Data Science selects on the Facebook page and looks at the users in the United States who have liked it and liked political candidates up for election this November. If the Facebook likes of Jennifer Hudson&#8217;s page (for example) come from users who have liked Democrats and not Republicans, that moves Jennifer Hudson&#8217;s entry further left.

Additional problems of interpretation arise.

  * Rather than look at self-identified Republicans or self-identified Democrats, Facebook&#8217;s Data Science blog looks at those who have liked &#8220;candidates&#8221;. No additional information about &#8220;candidates&#8221; is provided. We don&#8217;t know if the comparison rests on House candidates (who are all up for election), or Senate or gubernatorial candidates (who may be up for election). It&#8217;s conceivable that someone who likes Jerry Brown for Governor of California is someone who is otherwise a solid Republican. Brown is popular in California even among Republicans. The sampling frame is not clear.
  * A Facebook &#8220;like&#8221; does not mean what Facebook thinks it means. This is curious, because Facebook, of all entities, should know better. If I want to follow what Lindsey Graham is doing and have his updates appear in my news feed, I have to &#8220;like&#8221; him first. I may not &#8220;like&#8221; Lindsey Graham, but I have to &#8220;like&#8221; him if I want to keep easier track of him on Facebook. Beyond concerns of a sampling frame, there already issues of biased measurement. Would it not have been easier to make comparisons between people who linked their &#8220;political views&#8221; in their info to the two major parties for this purpose?
  * Facebook&#8217;s Data Science blog explains that larger fonts coincide with more Facebook likes. This lends itself to an interpretation that Democrats tend to like more &#8220;popular&#8221; artists like Lady Gaga and Eminem while Republicans like less mainstream (i.e. country) artists. However it&#8217;s worth repeating the individual Facebook user is not the unit of analysis and Facebook&#8217;s Data Science blog is inviting errors of fallacious inference. Ultimately, who cares? Graphs should be narrow in focus. I want to know about cultural differences between Republican users and Democrat users, not how popular Taylor Swift is.

To answer [Mother Jones&#8217; question][2]: it&#8217;s not that Republicans hate The Beatles. We don&#8217;t know that. At the most, that graph is showing that among the Facebook users in the United States who have liked The Beatles&#8217; Facebook page, more of them have also liked &#8220;Democratic candidates&#8221; versus &#8220;Republican candidates&#8221; (if I understand Facebook Data Science blog correctly). I have no doubt many ardent Republicans are jamming to &#8220;I Want to Hold Your Hand&#8221; on their iPod en route to class or work.

However, this interpretation is not particularly interesting, nor does it make for an appealing headline to generate traffic. So, we arrive at misinterpretations like this. Fault Facebook for not doing better in visualizing and presenting what data it has.

<ol class="footnotes">
  <li id="footnote_0_97" class="footnote">
    From my perspective, the more pressing question would be why doesn&#8217;t everyone love Mary J. Blige. She&#8217;s awesome, but alas. [<a href="#identifier_0_97" class="footnote-link footnote-back-link">&#8617;</a>]
  </li>
</ol>

 [1]: https://www.facebook.com/notes/facebook-data-science/politics-and-culture-on-facebook-in-the-2014-midterm-elections/10152598396348859?pnref=story
 [2]: http://www.motherjones.com/kevin-drum/2014/10/why-do-republicans-hate-beatles
 [3]: http://en.wikipedia.org/wiki/Scatter_plot
 [4]: https://www.facebook.com/notes/facebook-data-science/politics-and-culture-on-facebook-in-the-2014-midterm-elections/10152598396348859?comment_id=10152621374408859&offset=0&total_comments=39