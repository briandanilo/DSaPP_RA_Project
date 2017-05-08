dssg-evaluation

See comments in jupyter file for more data/analysis

# Exploratory analysis #
# Describe the dataset using counts, averages, frequency tables, and plots. Do you see anything interesting or potentially problematic? #

Just under 6% of projects are exciting. The hardest criterion to meet of the required four is at_least_one_teacher_referred_donor (true in only 24% of projects). Fully_funded is not hard to achieve (82% of projects are fully funded). I find this "low valuation of money" strange and a bit problematic (discussed further in "questions for the project partner") .

Some other comments/issues/findings: 

- the great_chat criterion seems inappropriate. Wouldn't the value of a robust comment section / donor enthusiasm be priced into dollars raised and the quality of donors/donations (green or not, new or not, etc)? Is leaving a message a very strong predictor of likelihood to donate again (and not already captured by other donor metrics)? 

- some not suprising findings: charter schools do very well, and poor schools dont. these are not mutually exclusive (plenty of charter schools serve poor areas), but i would guess that charter schools (being private) are generally superior to (exclusively public) magnet schools. magnet schools do better than average, but far worse than charter schools. being public, i suspect they poorer and are somehow hampered by america's awful education system (can't pay teachers enough, etc). 

- Teach For America (TFA) projects are much more likely to be exciting than NY Teaching Fellows (NYTF). Interesting-- they are both similar programs.   

# A Data Story #
# Find a specific interesting case in the data and tell us what happens with it. Provide evidence from the data that supports your narrative #

TFA and NYTF are similar programs (recruiting talented new teachers), yet TFA projects are exciting 11.8% of the time, whereas NYTF is only 5.8%.  Initially I thought this was due to NYTF asking for more expensive materials (and thus failing more because they have a harder task in raising more money), but this does not fit with my earlier finding that getting fully funded is actually fairly easy.  Also, when you exclude the most expensive 10% of projects, NYTF actually asks for cheaper projects, but still succeds only about half as often as TFA. And, in fact, NYTF is fully_funded 94% of the time to TFA's 92% (again, excluding top 10% most expensive projects)

The reason that NYTF is not as likely to be exciting is that they are weak on donor and engagement KPIs.  The hardest criterion to meet (at_least_one_teacher_referred_donor) explains much of this disparity. NYTF teachers are only about half as likely to acquire a new donor. More data in the notebook, but you'll see that NYTF gets higher quality donors, but fewer of them.  

# Questions for the Project Partner #
# What questions would you ask the partner now that you have seen the data? What is missing that you might need to get from them or other data sources to do something useful with the data? #

One big question is: what happens to the money if the project isn't fully funded? Is it like kickstarter where it goes back to the donors? If not, fully_funded might not be a great metric, since a project that gets $99 out of $100 is being treated the same as a project that gets $50 out of $100.

Do they have lifetime value metrics? I'd want to quantify the donor acquisition metrics. They distinguish between types of donors acquired by a project (teacher referred or non, donates more than 100 or not, great chat or not).  Instead of all these binary data points, why not give them numeric value (e.g. instead of great_chat = t or f, have it equal to something like the dollar amount that you can expect in future donations from a donor who made a great chat).  Then, instead of evalauting a project on is_exciting t/f, simply evaluate the total value to the business of a project (dollars raised + future dollars expected from these donors - adjustments for non cash donations). It seems very strange to me that a fundraising organization's chief KPI is not dollars raised, but rather a hybrid of dollars raised and various qualities of the donors (great chat, etc) which of course ultimately boils down to more dollars raised in the future.   

# Modeling #
# For those applying for machine learning positions #
I am interested in working on machine learning but ran out of time. I don't have any experience with this, but would be able to study quite a bit before my first day.
