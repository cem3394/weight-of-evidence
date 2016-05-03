
![](bletchley.jpg)
<br>
<br>

"In so far as a scientific statement speaks about reality, it must be falsifiable; and in so far as it is not falsifiable, it does not speak about reality."

* [Karl Popper](https://en.wikipedia.org/wiki/Karl_Popper) 

---


#Frequentist vs Bayesian Probability

In the frequentist view, probabilities represent long run frequencies of events.
$$
$$
In the Bayesian view, probability is used to quantify our uncertainty about something; hence it is fundamentally related to information theory.
$$
$$
One big advantage of the Bayesian interpretation is that it can be used to model our uncertainty about events that do not have long term frequencies or otherwise fit into a frequentist paradigm

---

Leicester City FC won the Premiere League Championship in 2015-16. It was quite an [amazing story](https://www.reddit.com/r/sports/comments/44w18p/if_you_are_not_watching_the_premier_league_here/).

[William Hill](http://sports.williamhill.com/bet/en-gb), an England-based sportsbook, had the Foxes as 5,000:1 long shots to win the Premier League before the 2015-16 season

---

#How Crazy is 5,000:1?

Here are some other bets (legal in England, not the U.S.) that were offered at those same odds by William Hill in August of 2015:

* Elvis is found alive.
* Christmas 2015 is the warmest day of the year in England.
* Kim Kardashian becomes the U.S. president in 2020.
* Barack Obama plays cricket for England after he leaves Oval Office.

---

![](lc-odds.png)
<center> [source](https://www.reddit.com/r/dataisbeautiful/comments/4dm169/odds_on_leicester_to_win_the_premier_league_after/)</center> 


---

#Bayes' Theorem V1

$$
p(H | E) = \frac{p(E | H) p(H)}{p(E | H) p(H) + p(E | ~H) p(~H)}
$$

---


#Challenge Question

Suppose that there are two duffel bags, each containing a number of \$1,000 casino chips.  In both bags, 40% of the chips are valuable and the rest are counterfeit.  Futhermore, in both bags, some chips are from Ceasar's Palace and the rest are from Harrah's.  
<br>
<br>
In the first bag, 30% of the real chips are Ceasar's, and 10% of the counterfeit chips are Ceasar's. In the second bag,  90% of the real chips are Ceasar's, and 30% of the counterfeit chips are Ceasar's.  
$$
$$
Would you rather have a Ceasar's chip from the first or second bag?  Would you rather have a Harrah's chip from the first or second bag?

---

---


$p(real|Ceasar's)$ and $p(real|Harrah's)$ have two degrees of freedom among them even when $p(real)$ is fixed - so there's no reason why one quantity shouldn't change while the other remains constant. 
$$
$$
In the second bag, the proportion of Ceasar's chips that are real is the same as in the first bag, but a much larger fraction of the chips are from Ceasar's.  This alters the set of Harrah's chips in such a way that the proportions do in fact change.  


---

#Liklihood Ratios

The probability that a test gives a true positive divided by the probability that a test gives a false positive is known as the likelihood ratio of that test: 
$$
\frac{p(E | H)}{p(E | ~H)}
$$


---


#Bayes' Theorem V2

$$
\frac{p(H)}{p(~H)} * \frac{p(E | H)}{p(E | ~H)} = \frac{p(H | E)}{p(~H | E)}
$$

---

The likelihood ratio $p(E | H) / p(E | ~H)$, determines how much observing $E$ slides the probability for $H$, i.e. the strength of $E$ as evidence for $H$.  
$$
$$
This tells us everything there is to know about the meaning of a positive result.  But it doesn't tell us the meaning of a negative result, and it doesn't tell us how often the test is useful.  

---

For example, a mammography with a hit rate of 80% for patients with breast cancer and a false positive rate of 9.6% for healthy patients has the same likelihood ratio as a test with an 8% hit rate and a false positive rate of 0.96%.  Although these two tests have the same likelihood ratio, the first test is more useful in every way - it detects disease more often, and a negative result is stronger evidence of health.

---

#[Banburismus](https://en.wikipedia.org/wiki/Banburismus)

[I.J. Good](https://en.wikipedia.org/wiki/I._J._Good) and Alan Turing were the first to suggest that credibility and evidence should be measured in decibels, or [bans](https://en.wikipedia.org/wiki/Ban_(unit)). 
$$
$$
The ban is a measure of the weight of evidence in favour of a hypothesis, usually applied [sequentially](https://en.wikipedia.org/wiki/Sequential_analysis).
$$
$$
It is essentially the same measure as a bit ($1$ ban $= \log_2(10)$ bits), though the ban predated Shannon's bit by about eight years.

---

#Decibels?

[Decibels](https://en.wikipedia.org/wiki/Decibel) are widely used in engineering for measuring exponential differences of intensity.  
$$
$$
Thus, the ratio of $P$ (measured quantity) to $P_0$ (context-dependent baseline reference quantity) expressed my a decibel quanity $L_P$:

$$
L_P= 10 \log_{10}(\frac{P}{P_0})
$$

---

For example, if the sound from an automobile horn carries 10,000 times as much energy (per square meter per second) as the sound from an alarm clock, the automobile horn would be 40 decibels louder.  
<br>
<br>
The sound of a bird singing might carry 1,000 times less energy than an alarm clock, and hence would be 30 decibels softer.  

---

![](img/log-odds.png)

---


<table style="width: auto; border: 1px solid #ddd; margin: 1px auto;" align="center">
<tbody>
<tr>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div><strong>Chances of&#8230;<br />
</strong></div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div><strong>Probability</strong></div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div><strong>Odds</strong></div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div><strong>Log-odds<br />
</strong></div>
<div>(in decibans)</div>
</td>
</tr>

<tr>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>A ticket winning the<br />
Grand Prize in the<br />
Powerball Lottery<a class="fn-ref-mark" href="http://www.powerball.com/powerball/pb_prizes.asp" id="refmark-4"><sup>[4]</sup></a></div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>0.000000571%</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div style="text-align: left;">1 : 175,223,510</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>-82.44</div>
</td>
</tr>

<tr>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>Being dealt a<br />
royal flush in poker</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>0.00015%</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>1 : 649,739</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>-58.1</div>
</td>
</tr>

<tr>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>Rolling a twelve<br />
with two 6-sided dice</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>2.78%</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>1 : 35</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>-15.4</div>
</td>
</tr>

<tr>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>A fair coin landing<br />
on heads</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>50.0%</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>1 : 1</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>0</div>
</td>
</tr>

<tr>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>At least one head<br />
in ten coin flips</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>99.9%</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>1023 : 1</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>30.1</div>
</td>
</tr>

<tr>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>At least one birthday<br />
shared in a group of<br />
100 random people</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>99.99997%</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>3,254,689 : 1</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>65.1</div>
</td>
</tr>

<tr>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>Surviving 1km of travel<br />
on Canadian roads<a class="fn-ref-mark" href="https://www.tc.gc.ca/eng/motorvehiclesafety/tp-1317.htm" id="refmark-5"><sup>[5]</sup></a></div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>99.99999934%</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>151,515,151 : 1</div>
</td>
<td style="vertical-align: top; border: 1px solid #ddd; padding: 10px;">
<div>81.8</div>
</td>
</tr>

</tbody>
</table>

---

Suppose we start with a prior probability of 1% that a woman has breast cancer, corresponding to an odds ratio of 1:99.  And then we administer three tests of likelihood ratios 25:3, 18:1, and 7:2.  

\begin{align} 
10 & \log_{10}(1/99) = -20
\newline
10 &\log_{10}(25/3) = 9
\newline
10 &\log_{10}(18/1) = 13
\newline
10 &\log_{10}(7/2)  = 5
\newline
\end{align} 

---

It starts out as fairly unlikely that a woman has breast cancer - our credibility level is at -20 decibels.  
<br>
<br>
Then three test results come in, corresponding to 9, 13, and 5 decibels of evidence.  
<br>
<br>
This raises the credibility level by a total of 27 decibels, meaning that the prior credibility of -20 decibels goes to a posterior credibility of 7 decibels.  
<br>
<br>
So the odds go from 1:99 to 5:1, and the probability goes from 1% to around 83%.

---

#Challenge Question

In front of you is a bookbag containing 1,000 casino chips.  I started out with two such bookbags, one containing 700 red and 300 blue chips, the other containing 300 red and 700 blue.  I flipped a fair coin to determine which bookbag to use, so your prior probability that the bookbag in front of you is the red bookbag is 50%.  
$$
$$
Now, you sample randomly, with replacement after each chip.  In 12 samples, you get 8 reds and 4 blues.  How many decibels of evidence are there for the hypothesis that this is the predominantly red bag? What are the posterior odds?


---



#Falsification 


If $p(E|H) ~ 1$ (i.e. the hypothesis makes a definitive prediction) - then observing $~E$ very strongly falsifies $H$.  
$$
$$
However if $p(E|H) ~ 1$,  and we observe $E$, this doesn't definitely confirm the hypothesis; there might be some other condition $G$ such that $p(E|G) ~ 1$, in which case observing $E$ doesn't favor $H$ over $G$.  

---

For observing $E$ to definitely confirm $H$, we would have to know, not that $p(E|H) ~ 1$, but that $p(E|~H) ~ 0$, which requires ranging over all possible alternative explanations. 
$$
$$
In other words hypotheses can be definitely falsified, but never definitely confirmed.
$$
$$
This is sometimes referred to as the [black swan fallacy](https://en.wikipedia.org/wiki/Falsifiability).

---

Assume that some piece of evidence $F$ is highly unlikely under hypothesis $H$, then $p(F|H)$ is infinitesimal and the likelihood ratio will also be infinitesimal. 
$$
$$
For example, if $p(F|H) = 0.000001$, and $p(F|~H) = 0.01$, then the likelihood ratio $p(F|H)/p(F|~H)$ will be 1:10000.  
$$
$$
This amounts to $-40$ decibels of evidence, meaning that observing $F$ greatly favors $~H$ over $H$.  



---
 
