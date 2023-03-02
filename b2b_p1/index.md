# Back2Basics P.1 - e and log

# The *e*

You probably have heard the saying that "there is no force in the universe more powerful than compound interest". It was supposedly said by Albert Einstein. The saying could be an urban legend but it points out the importance of the concept called exponential growth. Einstein could have said "there is no force in the universe more powerful than exponential growth" and he would have made the same point but I think there is this slight difference between a natural phenomenon displays exponential growth and compound interest when it comes to the point of growing exponentially forever. Anyway, when we talk about exponential growth or exponentials in general, the number e pops up naturally. In this blog post I'll try discover e.

What is e? If you have taken maths course you must have heard it but have you ever think on it? How to get this magical number? And most importantly, why this number has a special name?

The number e, also known as Euler's number which is approximately equals to 2.7183. I said approximately because like $\pi$ it goes on forever. I will not get into historical bits who found it etc. Doesn't matter for me, what I want is to find or discover this number myself and by doing so, I want to understand it as much as I can do. And since this blog is also about quantitative mathematics, I will try to do it in context of finance.

Let's start with a simple question. Assume that I have found a bank which pays 100% interest (yep) annually for my deposit. If I deposit a dollar to the bank , how much money would I have the next year? It is simple let's work it out.
$$M_{1} = 1 * (1 + 1)$$

Now, start thinking about increasing the times that the bank applies the interest. What if the bank compounds the interest twice a year? 
$$M_{1} = 1 * (1 + \frac{1}{2})^2$$

In this case, the money would be 2.25 dollars. The extra bit is actually the interest made over the interest. What if we do this every day?
$$M_{1} = 1 * (1 + \frac{1}{360})^{360}$$

It would be about 2.7145 What if we do this every minute or every second? The logical conclusion is the continuos compounding.
$$M_{1} = 1 *  \lim_{n\to\infty} (1 + \frac{1}{n})^n $$

In other words, we are breaking that one year into infinitely many small chunks and compound on every single one of them and adjusting the rate accordingly. What would we get at the end of the year? Let's try to figure out approximately by putting large numbers to n.

* For n=100,000, $M_{1} \approx 2.7182$
* For n=1,000,000, $M_{1} \approx 2.7182$
* For n=10,000,000, $M_{1} \approx 2.7182$
* For n=100,000,000, $M_{1} \approx 2.7183$

You could see yourself that it doesn't change much and the the amount of money sort of approximated to a value which roughly equals to 2.7183. Let's call this number e, okay? Basically we are establishing this:
$$e = \lim_{n\to\infty} (1 + \frac{1}{n})^n $$

You can work out this limit yourself to actually get e but what we have done should be pretty close how e was discovered in the first place.

What if we change the interest rate? Let's say the annual interest rate is 5%. We definately going to get smaller return in this case but can we get the number e from that as well? I give the results below.

* For n=1, $M_{1} = 1.05$
* For n=2, $M_{1} = 1.0506$
* For n=1,000, $M_{1} \approx 1.0512$
* For n=1,000,000, $M_{1} \approx 1.0512$
* For n=1,000,000, $M_{1} \approx 1.0512$
* For n=100,000,000, $M_{1} \approx 1.0512$

e was about continuous compounding so look to the large values of n. The money again converges to a value which is 1.0512 and also equals to $e^{0.05}$. Therefore we get this for any interest rate.

$$e^{r} = \lim_{n\to\infty} (1 + \frac{r}{n})^n $$

If we put all this into words, for a dollar, if your interest compounds continuously and your rate is r for a period, after a period your money grows into $e^{r}$. After two periods it is $e^{2r}$, so on and so forth.

So far, we've discovered the number e ourselves. $e^{r}$ or $e^{x}$ in general, is a function of a value $x$, which is simply e raised to the power x. What is special about $e^{x}$ is the gradient of the function is also $e^{x}$. Rate of change of the function is the function itself.

## log

Think of log as the inverse of e, in a sense. Basically,
$$ e^{lnx} = x $$

In the last example we found that $e^{0.05}$ is equals to 1.0512. So, we can say that $ln(1.0512) = 0.05$. Of course, this is denoted in base $e$. You can write logarithms in different bases like 10 for example.

As a conclusion, we've seen that e naturally pops up when things grow continuously and rate of change is proportional to itself.
