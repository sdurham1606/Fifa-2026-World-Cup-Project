This markdown file will go through every graph/plot in the 05_EDA notebook and explain our findings.

05_EDA_plot_01: 2026 World Cup - Win Rate of the 15 Teams with Greatest Tournament Progression / Win Rate 

This bar chart compares the win rates of 15 teams selected by tournament progression and win rate. Win rate represents 
the proportion of matches a team won. 
The chart helps establish which teams were successful before investigating the characteristics associated with that success. 
Argentina and Spain had the highest win rates among the displayed teams, both at 87.5%. England and France followed at 75%. 
This demonstrates that tournament success varies substantially between teams. However, win rate and tournament progression 
are not identical.

05_EDA_plot_02: 2026 FIFA Rank vs 2026 World Cup Win Rate 

The scatterplot compares each teams FIFA ranking with its 2026 World Cup win rate. A lower ranking number represents a stronger 
FIFA ranking. 
From the plot we can deduce that there is a strong negative relationship between numerical FIFA ranking and win rate. 
Better ranked teams generally achieved higher win rates. 
The relationship is not perfect, which means ranking alone cannot explain each team's performance. 

05_EDA_plot_03: 2026 FIFA Rank vs Tournament Progression 

This graph compares FIFA ranking with the number of World Cup matches played. The notebook uses matches played as an approximate 
indicator of tournament progression, because teams advancing further play more matches. 
The conclusion we can make from this? Better-ranked teams generally played more tournament matches, suggesting stronger teams tended to 
progress further. The correlation however is weaker than the relationship between FIFA ranking and win rate (-0.710). 
This shows that FIFA ranking is associated with both winning matches and progressing through the tournament, although 
these are different measures of success. 

05_EDA_plot_04: Attacking Performance: Shot Volume vs Shot Conversion 

These two scatter plots compare different aspects of attacking performance with win rate. The left graph examines attempts at 
goal per match, while the right graph examines the percentage of attempts converted into goals.
Shot volume per match had a correlation of approx. 0.53 with win rate, compared with approx 0.46 for shot conversion. 
Both are positive correlations, but shot volume is slightly higher. This may suggest that teams creating more shooting opportunities 
tend to achieve greater success, although finishing efficiency also matters. 

05_EDA_plot_05: Defensive Performance - Goals conceded and clean sheets

The left scatter plot compares goals conceded per match with win rate. The right is for clean-sheet rate with win rate. 
Goals conceded per match had a negative correlation of minus 0.60, while clean-sheet rate had a positive correlation of 0.51. 
This suggests that teams with stronger defensive records generally achieve higher win rates. 
It also highlights that successful teams need more than attacking strength. Preventing goals is an important part of tournament performance. 

05_EDA_plot_06: Selected 2026 Performance Metrics - Correlation with Win Rate

This bar chart compares correlations between win rate and additional performance characteristics, including passing, movement, 
physical performance and discipline. 
Passing accuracy, offers to receive and defensive line-break accuracy have relatively strong positive relationships with success. 
By comparison, sprint frequency and average speed show much weaker relationships. 
This suggests that technical execution and movement may be more closely associated with success than simply covering ground or sprinting frequently. 

05_EDA_plot_07: Mean 2026 World Cup Win Rate by Confederation 

We compared the average win rates of teams across the 6 FIFA confederations. 
UEFA had the highest average win rate at 46%, closely followed by CONMEBOL at 42%. 
However, the number of participating teams differed considerably between regions. 
Therefore, these findings describe regional patterns in this tournament rather than proving that a particular confederation gives 
teams an advantage. 

05_EDA_plot_08: Match Outcome after scoring the first goal

This chart shows the final outcomes of 974 historical World Cup matches in which the first goalscorer could be identified. 
We found that the first-scoring team went on to win approximately 71% of the time, while only 13% went on to lose. 
This suggests that taking the lead is strongly associated with winning, although other factors, including the relative strength of the teams, 
may also contribute. 

05_EDA_plot_09: Win rate after scoring first, by first goal timing. 

This chart investigates whether the timing of the opening goal is associated with the likelihood that the first 
scoring team wins. 
Teams scoring first the opening 15 minutes won approximately 66% of their matches. 
In comparison, teams scoring first between minutes 76 and 90 won approximately 92%. 
One possible explanation is that opponents have less time to respond to a late goal. 
However, the later categories contain fewer matches, so these percentages should be interpreted with some caution. 

05_EDA_plot_10: World Cup matches containing penalty goals or own goals 

We also examined how frequently penalty goals ad own goals occurred in historical World Cup matches. 
We found that approximately 19% of matches contained a penalty goal, compared with just 6% containing an own goal. 
This shows that penalty goals were more common than own goals. 
However, this analysis focuses on how frequently these events occurred, rather than measuring their direct impact on the final 
result. 

05_EDA_plot_11: Penalty shootout outcome when first shooter is known

We investigated whether the team taking the first penalty in a shootout was more likely to win. 
Out of the 260 shootouts where the first shooter was known, the first shooting team won 52.3%. 
This was only slightly above 50%, suggesting that any advantage was relatively small in our observed data. 
However, first-shooter information was available for only 38% of shootout records, so we cannot draw a strong conclusion from this alone. 

05_EDA_plot_12: Selected factors associated with 2026 world cup win rate 

After examining the individual performance areas, we combined the selected metrics into one correlation overview.
Expected goals showed the strongest positive relationship with win rate, followed by shots on target and passing accuracy.
FIFA ranking and goals conceded also showed relatively strong negative correlations.
These results suggest that World Cup success is associated with several aspects of performance, rather than one individual characteristic.
However, some measures, such as cumulative expected goals, may also reflect how far a team progressed, 
so the relationships should not be interpreted as causal.

05_EDA_plot_13: Strength of association with 2026 win rate - Attack vs Defense

This graph compares the absolute correlations of four attacking and defensive measures with win rate. 
Goals scored per match had the strongest relationship with win rate, with a correlation of 0.71. 
Goals conceded per match followed with an absolute correlation of 0.60, while clean-sheet rate and shot conversion showed slightly weaker relationships. 
This suggests that attacking output was particularly strongly associated with success in our dataset, although defensive 
performance was also important. 





