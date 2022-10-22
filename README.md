# STAT108-PROJECT






## Introduction

After the U.S. Supreme Court decides to overrule Roe v. Wade (1973) which guaranteed a constitutional right to abortion services, abortion and reproductive rights will be dependent on each state's judgment starting June 2022 and it is expected that half of the states in the United States will outlaw abortions (Smith et al., 2022).

Before this, even though abortion was made legal, most states have implemented regulations promoting abortion scarcity and leading to barriers to care in recent decades (Wolfe & van der Meulen Rodgers, 2021). For instance, Texas' House Bill 2 and Louisiana law required all abortion providers to maintain admitting privileges at a nearby hospital (Arnold, 2022). It's crucial to highlight the similar but more restrictive forms of laws commonly known as "Targeted Regulation of Abortion Providers" (TRAP) Laws that put stringent and unnecessary requirements on abortion providers (Austin & Harper, 2018). In 2017, 89% of counties in the United States have no abortion providers within their borders. People were forced to travel more than 100 miles to receive abortion services as of 2018 in 27 cities (Smith et al., 2022).

Even while laws are widespread, few studies accessing the impact of such regulations on abortions and fertility. For instance, Ellertson (1997) found a decrease in the in-state abortion rate and delay in abortions when parental involvement laws took effect, which implies the increased odds of traveling out of state for abortions. Also, Addante et al. (2021) concluded that states with more restrictive abortions have higher maternal mortality than states with moderate or protective abortions. Such scarcity of research is particularly noteworthy after the overturn of Roe v. Wade, which emphasized the importance of providing solid evidence-based research on the potential impact of regulations restricting access to abortion care (Arnold, 2022).

At the same time, COVID-19's introduction into a climate of abortion restrictions has increased the difficulties that providers and communities already face (Wolfe & van der Meulen Rodgers, 2021). **Our study sought to assess the difference in abortion access and rate before and during COVID-19 and examine the impact of abortion barriers on abortion and fertility outcomes.** We hypothesize that increased barriers to care might result in a decrease in the in-state abortion rate and an increase in maternal mortality rate, but potentially an increase in traveling across state lines for abortion care.

## Data Collection

### Abortion and fertility data

The two main sources for abortion data is the Centers for Disease Control (CDC) and the Alan Guttmacher Institute (AGI). CDC is the national public health federal agency of the United States. AGI is a leading research and policy NGO committed to advancing sexual and reproductive health starting in 1968.

Dataset from CDC reports the number of abortion incidence and rate by state of occurrence in 2017, 2019, and 2020. Each year, CDC requests abortion data from the central health agencies for 50 states, the District of Columbia, and New York City. Dataset from AGI contains the number of abortion incidence and rate by state of occurrence and state of residence in 2020. AGI collects information by conducting a direct survey of abortion providers for each state beginning in 1973.

### Abortion care and policy data

The dataset for abortion care is collected from the Abortion Facility Database Project, Advancing New Standards in
Reproductive Health (ANSIRH), at University of California San Francisco. It mainly provides the number of women of reproductive age per facility, gestational limit, and median cost of abortion services from 2017 to 2021. Data is offered by publicly advertising facilities across the United States from 2018 through 2021.

The source for state abortion policy is AGI, which was collected from the American Community Survey. States were scored based on whether they had policies in effect in any of six categories of abortion restrictions and any of six categories of measures that protect or expand abortion rights and access. Each state was given a score of 1 for every protective measure in effect and a score of -1 for every abortion restriction in effect. A state with a score of either positive or negative six has either all of the abortion restrictions or all of the protective measures in effect.



```{R}
glimpse(read.csv("data/abortion_data.csv"))
```



## References

Addante, A. N., Eisenberg, D. L., Valentine, M. C., Leonard, J., Maddox, K. E. J., &amp; Hoofnagle, M. H. (2021, March 26). 
_The association between state-level abortion restrictions and maternal mortality in the United States, 1995-2017._
Contraception. 
https://www.sciencedirect.com/science/article/pii/S0010782421000901 

Arnold, G. (2022, May 30). 
_The impact of targeted regulation of abortion providers laws on abortions and births - Journal of Population Economics._
SpringerLink. 
https://link.springer.com/article/10.1007/s00148-022-00903-3 

Austin, N., &amp; Harper, S. (2018, April 1). 
_Assessing the impact of trap laws on abortion and women's health in the USA: A systematic review._ 
BMJ Sexual &amp; Reproductive Health. 
https://srh.bmj.com/content/44/2/128.abstract 

Ellertson, C. (1997, August). 
_Mandatory parental involvement in minors' abortions: Effects of the laws in Minnesota, Missouri, and Indiana._
American journal of public health. 
https://pubmed.ncbi.nlm.nih.gov/9279279/ 

Smith, E., Ortiz, J., Thanhauser, L., Gray, A., Akpaka, N., Chowdhry, N., Jorawar, S., &amp; Pelka, A. (2022, August 25). 
_Abortion laws by State._ 
Center for Reproductive Rights. 
https://reproductiverights.org/maps/abortion-laws-by-state/ 

Wolfe, T., &amp; van der Meulen Rodgers, Y. (2021, March 22). 
_Abortion during the COVID-19 pandemic: Racial disparities and barriers to care in the USA - Sexuality Research and Social Policy._ 
SpringerLink. 
https://link.springer.com/article/10.1007/s13178-021-00569-8 

Wolfe, T., &amp; van der Meulen Rodgers, Y. (2021, March 22). 
_Abortion during the COVID-19 pandemic: Racial disparities and barriers to care in the USA - Sexuality Research and Social Policy._ 
SpringerLink. 
https://link.springer.com/article/10.1007/s13178-021-00569-8 
