## Research Question

Examining the impact of state-level restrictive regulations on abortions
in the United States.

## Introduction

After the U.S. Supreme Court decides to overrule Roe v. Wade (1973)
which guaranteed a constitutional right to abortion services, abortion
and reproductive rights will be dependent on each state’s judgment
starting June 2022 and it is expected that half of the states in the
United States will outlaw abortions (Smith et al., 2022).

Before this, even though abortion was made legal, most states have
implemented regulations promoting abortion scarcity and leading to
barriers to care in recent decades (Wolfe & van der Meulen Rodgers,
2021). For instance, Texas’ House Bill 2 and Louisiana law required all
abortion providers to maintain admitting privileges at a nearby hospital
(Arnold, 2022). It’s crucial to highlight the more restrictive forms of
laws commonly known as “Targeted Regulation of Abortion Providers”
(TRAP) Laws that put stringent and unnecessary requirements on abortion
providers (Austin & Harper, 2018). In 2017, 89% of counties in the
United States have no abortion providers within their borders. People
were forced to travel more than 100 miles to receive abortion services
as of 2018 in 27 cities (Smith et al., 2022).

Even while laws are widespread, few studies assessed the impact of such
regulations on abortions and fertility. For instance, Ellertson (1997)
found a decrease in the in-state abortion rate and delay in abortions
when parental involvement laws took effect, which implies the increased
odds of traveling out of state for abortions. Also, Addante et
al. (2021) concluded that states with more restrictive abortions have
higher maternal mortality than states with moderate or protective
abortions from 1995 to 2017. Most articles evaluate policy effects from
2006 or earlier, possibly prior to the more recent surge in regulation
enactment (Austin & Harper, 2018). Such scarcity of research is
particularly noteworthy after the overturn of Roe v. Wade, which
emphasized the importance of providing solid evidence on the impact of
regulations restricting access to abortion care in light of contemporary
policy shifts (Arnold, 2022).

Our study sought to examine the impact of abortion barriers on abortion
rate and cross-state movement to obtain abortion care from 2017 to 2019
in the United States. We hypothesize that increased barriers to care
might result in a decrease in the in-state abortion rate, but an
increase in traveling across states for abortion care.

## Data Collection

### Abortion rate and cross-state movement to obtain abortion care

We rely on data from CDC’s annual Abortion Surveillance report for our
analysis of abortion rate and interstate travel for abortion care. CDC
is the national public health federal agency of the United States.
Starting from 1969, they compile information from reporting areas to
produce national estimates of legal induced abortions. They report the
number of abortion incidence by state of residence and state of clinical
service. Additionally, four states (California, Maryland, New Hampshire,
and Wyoming) either did not report to the CDC, or did not conform to
reporting requirements, therefore are not included in the analysis.

We use the total number of abortion by state of residence to calculate
abortion rate, and the number of abortion where states of residence and
clinical services are the same to calculate percentage of leaving.

### Abortion policy and abortion care

The source for state abortion policy is AGI, which was collected from
the American Community Survey. States were scored based on whether they
had policies in effect in any of six categories of abortion restrictions
and any of six categories of measures that protect or expand abortion
rights and access. Each state was given a score of 1 for every
protective measure in effect and a score of -1 for every abortion
restriction in effect. A state with a score of either positive or
negative six has either all of the abortion restrictions or all of the
protective measures in effect.

The dataset for abortion care is collected from the Abortion Facility
Database Project, Advancing New Standards in Reproductive Health
(ANSIRH), at University of California San Francisco. It mainly provides
the number of women of reproductive age per facility, gestational limit,
and median cost of abortion services from 2017 to 2021. Data is offered
by publicly advertising abortion facilities across the United States.

Other risk factors, including percentage of poverty, are collected from
United States Census Bureau. The data includes the percentage of poverty
of 2-year average, which is based from Current Population Survey and
1960 to 2021 Annual Social and Economic Supplements (CPS ASEC). For each
year, we use the 2-year percentage of poverty from last year and the
corresponding year. For instance, the percentage of poverty in 2019 is
the average percentage of poverty in 2018 - 2019.

    glimpse(read.csv("data/new_abortion_data.csv"))

    ## Rows: 153
    ## Columns: 20
    ## $ X.1                          <int> 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13…
    ## $ X                            <int> 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13…
    ## $ State                        <chr> "Alabama", "Alabama", "Alabama", "Alaska"…
    ## $ year                         <int> 2017, 2018, 2019, 2017, 2018, 2019, 2017,…
    ## $ policy_index                 <int> -5, -5, -5, 2, 2, 2, -6, -6, -6, -6, -6, …
    ## $ abortion_rate_residence      <dbl> 6.65491545, 7.15497635, 7.12910538, 8.484…
    ## $ percentage_leaving           <dbl> 29.2372307, 31.1932392, 37.0295273, 11.32…
    ## $ facility_density             <dbl> 0.4508139, 0.4512472, 0.2710343, 3.649102…
    ## $ facilities_only_procedural   <int> 20, 20, 33, 0, 0, 0, 0, 0, 0, 0, 0, 0, 3,…
    ## $ facilities_only_medication   <int> 0, 0, 0, 17, 17, 17, 13, 13, 13, 67, 67, …
    ## $ facilities_both              <int> 80, 80, 67, 83, 83, 83, 88, 88, 88, 33, 3…
    ## $ gestational_limit_medication <int> 9, 9, 9, 10, 10, 10, 10, 10, 10, 9, 9, 9,…
    ## $ gestational_limit_procedural <int> 14, 14, 21, 14, 14, 14, 17, 17, 17, 21, 2…
    ## $ cost_medication              <int> NA, 525, 575, 800, 650, 800, NA, 460, 590…
    ## $ cost_first_trimester         <int> NA, 500, 500, 835, 650, 800, NA, 480, 620…
    ## $ cost_second_trimester        <int> NA, 650, NA, NA, 750, NA, NA, 1703, NA, N…
    ## $ accepts_insurance            <int> 40, 40, 33, 100, 100, 83, 38, 38, 63, 67,…
    ## $ independent_clinics          <int> 60, 60, 100, 33, 33, 33, 50, 50, 50, 33, …
    ## $ planned_parenthoods          <int> 40, 40, 0, 67, 67, 67, 50, 50, 50, 67, 67…
    ## $ poverty                      <dbl> 16.1, 15.6, 14.4, 11.8, 12.6, 11.7, 15.2,…

## References

Addante, A. N., Eisenberg, D. L., Valentine, M. C., Leonard, J., Maddox,
K. E. J., & Hoofnagle, M. H. (2021, March 26). *The association between
state-level abortion restrictions and maternal mortality in the United
States, 1995-2017.* Contraception.
<https://www.sciencedirect.com/science/article/pii/S0010782421000901>

Arnold, G. (2022, May 30). *The impact of targeted regulation of
abortion providers laws on abortions and births - Journal of Population
Economics.* SpringerLink.
<https://link.springer.com/article/10.1007/s00148-022-00903-3>

Austin, N., & Harper, S. (2018, April 1). *Assessing the impact of trap
laws on abortion and women’s health in the USA: A systematic review.*
BMJ Sexual & Reproductive Health.
<https://srh.bmj.com/content/44/2/128.abstract>

Centers for Disease Control and Prevention, National Center for Health
Statistics (NCHS), National Vital Statistics System, “*aternal deaths
and mortality rates: Each state, the District of Columbia, United
States, 2018‐2020*

Ellertson, C. (1997, August). *Mandatory parental involvement in minors’
abortions: Effects of the laws in Minnesota, Missouri, and Indiana.*
American journal of public health.
<https://pubmed.ncbi.nlm.nih.gov/9279279/>

Smith, E., Ortiz, J., Thanhauser, L., Gray, A., Akpaka, N., Chowdhry,
N., Jorawar, S., & Pelka, A. (2022, August 25). *Abortion laws by
State.* Center for Reproductive Rights.
<https://reproductiverights.org/maps/abortion-laws-by-state/>

Wolfe, T., & van der Meulen Rodgers, Y. (2021, March 22). *Abortion
during the COVID-19 pandemic: Racial disparities and barriers to care in
the USA - Sexuality Research and Social Policy.* SpringerLink.
<https://link.springer.com/article/10.1007/s13178-021-00569-8>
