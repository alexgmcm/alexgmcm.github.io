{% blockquote Sherlock Holmes %} When you have eliminated the
impossible, whatever remains, however improbable, must be the truth. {%
endblockquote %}

I recently discovered a neat problem while looking at job applications.
From the [Sparx Deck](http://sparx.co.uk/deck/fiendish/5.asp), the
problem is as follows:

{% blockquote %} A basketball player decides to spend an afternoon
practicing free throws and recording her performance. Over the first
hour, her scoring percentage is less than 75%, but by the end of the
session, her overall scoring percentage for the day is more than 75%. Is
it necessarily true that at some moment during the session her scoring
percentage was exactly 75%? {% endblockquote %}

<!-- more -->

The answer to the above problem is **yes**. This may seem
counter-intuitive but the reasoning will soon become clear as I was
interested in solving the extension: {% blockquote %} Extension: How
special is the choice of 75% in this question? Does the same result hold
for other percentages? {% endblockquote %}

So let us restate the general problem:

{% blockquote %} A basketball player decides to spend an afternoon
practicing free throws and recording her performance. Over the first
hour, her scoring percentage is less than p%, but by the end of the
session, her overall scoring percentage for the day is more than p%. Is
it necessarily true that at some moment during the session her scoring
percentage was exactly p%? {% endblockquote %}

To do this we will prove that the alternative, that the percentage can
skip over *p*%, must be false for some values of *p* and we will then
investigate what decides these values.

First let us express the percentage as a fraction \\(p=\frac{a}{b}
\times 100\\) subject to the constraint
\\(a<b\\) as it is impossible for the scoring percentage to exceed 100%.

If we assume that it is possible to skip over _p_ then there must be some point where the current percentage is less than _p_ but by scoring just one more basket it will exceed _p_.

If we let _B_ be the number of baskets scored and _N_ be the total number of shots attempted then we can express these requirements as:

\\[ \frac{B}{N}<\frac{a}{b} \quad \mathsf{ and } \quad \frac{B+1}{N+1}>\frac{a}{b}
\\]

These can be re-arranged to give: \\[ bB \< aN \\] \\[ b(B+1) \> a(N+1)
\\]

The latter of which can be rearranged to: \\[bB \>aN + a - b\\]

Remember we have the constraint that \\(a\<b\\), hence: \\[aN+a-b \<
aN\\]

Therefore we require that:

\\[ aN+a-b \< bB \< aN\\]

As we also require that *a*, *b*, *B* and *N* are all integers then
clearly this can only be satisfied when: \\[ a-b \< -1 \\]

In any case that \\(a-b = -1 \\) the scoring percentage will always pass
through *p* if it starts below it and ends up exceeding it.

For example this is the case for \\(p=75%\\) as \\(a=3\\) and \\(b=4\\)
but it is not the case for \\(p=60%\\) where \\(a=3\\) and \\(b=5\\).

Now we can see why it must pass through 75% and have determined the
other percentages for which this condition holds.
