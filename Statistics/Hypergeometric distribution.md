A distribution that is similar to [[Binomial distribution]], the only difference is that the trials are not required to be independent.
# Example
A deck of 52 cards. We wish to find 3 red cards out of 5 drawn. We cannot use the binomial distribution, since for it we need to put back the picked card and reshuffle the deck, which we do not do in this example. So, the hypergeometric distribution it is.

Let's find the probability of that happening:
1. We need to take 3 red cards out of 26 available, which is ${26 \choose 3}$
2. We need to take 2 black cards out of 26 available, which is ${26 \choose 2}$
3. We need to draw 5 cards out of 52 available, which is ${52 \choose 3}$
\1. and 2. must happen at the same time, so we multiply. This the probability of 3 red cards and 2 black cards. Now, we need to divide the number of all possible combinations on 5 cards, which is 3. So:
$$
\dfrac{{26 \choose 3} {26 \choose {2}}}{52 \choose 3} = \dfrac{26!/3!23!)(26!/2!24!}{52!/5!47!} = 0.3251
$$

