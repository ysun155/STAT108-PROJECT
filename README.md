## Examining the impact of state-level restrictive regulations on abortions in the United States.

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

At the same time, COVID-19’s introduction into a climate of abortion
restrictions has increased the difficulties that providers and
communities already face (Wolfe & van der Meulen Rodgers, 2021). Our
study sought to assess the difference in abortion access and rate before
and during COVID-19 and examine the impact of abortion barriers on
abortion and fertility outcomes. We hypothesize that increased barriers
to care might result in a decrease in the in-state abortion rate and an
increase in maternal mortality rate, but potentially an increase in
traveling across state lines for abortion care.

## Data Collection

### Abortion rate and maternal mortality rate

The main source for abortion data is the Alan Guttmacher Institute
(AGI), which is a leading research and policy nonprofit organization
committed to advancing sexual and reproductive health starting in 1968.
We collected abortion rate by state of occurrence, abortion rate by
state of residence, and percentage of travelling out of states for
abortion in 2020. AGI collects information by conducting a periodic
survey of abortion providers, Abortion Provider Census, for each state
beginning in 1973. With the number of abortions performed in each state
(abortions by state of occurrence) as estimated from the survey, they
reassigned abortions to patients’ states of residency using information
collected by state abortion reporting agencies.

Maternal mortality rate is collected from Centers for Disease Control
and Prevention (CDC), based from the National Vital Statistics System.
This dataset includes maternal mortality rate per 100,000 live births
from 2018 to 2020. Maternal deaths is defined to be deaths of women
while pregnant or within 42 days of termination of pregnancy,
irrespective of the duration and the site of the pregnancy, from any
cause related to or aggravated by the pregnancy or its management, but
not from accidental or incidental causes.

### Abortion policy and care data

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

Other risk factors, including education attainment and poverty, are
collected from FRED Economic Data and United States Census Bureau
respectively. The data about percentage of poverty of 2-year average
(2019-2020) is based from Current Population Survey and 1960 to 2021
Annual Social and Economic Supplements (CPS ASEC). Education attainment
data including percentage of High School Graduate or Higher and
Bachelor’s Degree of Higher in 2020 is based from the American Community
Survey.

    glimpse(read.csv("data/abortion_data.csv"))

    ## Rows: 51
    ## Columns: 23
    ## $ state                                 <chr> "Alabama", "Alaska", "Arizona", …
    ## $ abortion_rate_occurrence              <dbl> 6.0, 8.6, 9.3, 5.6, 19.2, 11.2, …
    ## $ abortion_rate_residence               <dbl> 9.5, 9.2, 9.7, 7.8, 19.0, 9.9, 1…
    ## $ percentage_of_travel                  <int> 47, 7, 6, 37, 0, 1, 6, 44, 45, 1…
    ## $ maternal_mortality_rate               <dbl> 36.202111, 27.232188, 28.264675,…
    ## $ policy_index                          <int> -5, 2, -6, -6, 6, 0, 3, -1, NA, …
    ## $ fertility_rate                        <dbl> 60.6, 65.7, 54.0, 60.7, 52.4, 51…
    ## $ facility_density                      <int> 368957, 32300, 201690, 335159, 5…
    ## $ change_open_facilities                <int> 0, -1, 0, -1, 4, 3, -6, 0, -1, -…
    ## $ facilities_only_procedural_abortion   <int> 33, 0, 0, 0, 2, 4, 0, 0, 0, 0, 0…
    ## $ Facilities_only_medication_abortion   <int> 0, 20, 13, 50, 54, 44, 50, 0, 0,…
    ## $ Facilities_both                       <int> 67, 80, 88, 50, 44, 52, 50, 100,…
    ## $ Gestational_limit_medication_abortion <int> 10, 11, 10, 11, 10, 11, 11, 11, …
    ## $ Gestational_limit_procedural_abortion <int> 21, 14, 17, 21, 18, 20, 17, 16, …
    ## $ cost_medication_abortion              <int> 525, 800, 605, 722, 680, 458, 65…
    ## $ cost_first_trimester                  <int> 500, 800, 620, 625, 700, 540, 76…
    ## $ cost_second_trimester                 <int> NA, 900, 1510, NA, 1170, 1500, 8…
    ## $ Accepts_insurance                     <int> 0, 80, 63, 0, 93, 74, 100, 100, …
    ## $ Number_of_independent_clinics         <int> 100, 20, 50, 50, 39, 48, 17, 0, …
    ## $ Number_of_Planned_Parenthoods         <int> 0, 80, 50, 50, 61, 52, 83, 100, …
    ## $ Bachelor_Degree                       <dbl> 27.8, 31.9, 33.0, 24.9, 36.9, 44…
    ## $ High_School                           <dbl> 88.0, 93.7, 89.1, 88.2, 84.4, 92…
    ## $ percentage_of_poverty                 <dbl> 13.9, 11.8, 10.4, 14.1, 10.6, 9.…

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

Wolfe, T., & van der Meulen Rodgers, Y. (2021, March 22). *Abortion
during the COVID-19 pandemic: Racial disparities and barriers to care in
the USA - Sexuality Research and Social Policy.* SpringerLink.
<https://link.springer.com/article/10.1007/s13178-021-00569-8>
