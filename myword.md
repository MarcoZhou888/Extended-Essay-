# Title: To what extent has the “National Pork Reserve” been effective in reducing price volatility in the Chinese hog market, given the counter-cyclical production strategies of oligopolistic suppliers between 2023 and 2025?

**Subject:** Economics  
**Word count:** [Insert Word Count]

---

## Table of Contents
1. Introduction
2. Methodology
3. Theoretical Framework & Policy Mechanism
    3.1 Cobweb Theorem
    3.2 Theoretical Policy Effects
        3.2.1 Scenario A: Price Floor Interventions During Oversupply
        3.2.2 Scenario B Price Ceiling Interventions During Shortages
4. Quantitative Analysis: Interrupted Time Series (ITS) Modeling
    4.1 Regression Results
    4.2 Coefficient Interpretations
        4.2.1 Phase 1: Speculative Bubble
        4.2.2 Phase 2: Inventory Liquidation and the Structural Crash
5. Qualitative Analysis: A Game Theoretical Model of Oligopolistic Moral Hazard
    5.1 Moral Hazard
    5.2 Prisoner’s Dilemma
6. Conclusion
7. Bibliography
8. Appendix

---

## 1. Introduction
Hogs are one of the most important livestock products in the Chinese economy. The price level in the hog market significantly influences national inflation by affecting farmers’ production decisions, consumers’ purchase behavior and the overall trend of market development (Zhou et al., 2024). The cyclical nature of the hog market is best described by the Cobweb theorem. which shows the fact that the time lag between production decision and harvest will create a mismatch between quantity demanded and quantity supplied, resulting in a cyclical hog price. 

Given the enormous effect hog price can have on the consumer price index, the inflation rate is extremely vulnerable to a volatile price fluctuation. Beyond inflation, the cyclical price volatility causes more risks such as unstable producer profitability, forced-exit of small-scale producers and the misallocation of production resources (Zhang et al., 2025). In order to mitigate these risks, the Chinese National Development and Reform Commission (NDRC) introduced the “National Pork Reserve” mechanism in June 2021. Generally, the mechanism functions as market absorption by buying up excess supply, or increasing market supply artificially by strategic reserve releases under certain circumstances. 

However, the effectiveness of such economic interventions has long been a topic of debate. While there were numerous studies on the effectiveness of the “National Pork Reserve” mechanism (e.g., Xiong et al., 2021 and Li et al., 2025), the majority of research focuses on the early stage of the policy (2021 - 2022), where the macroeconomic environment was distorted by COVID 19, alongside the impact on hog production due to the African Swine Fever (ASF). Few studies have examined the policy under a normalized post-pandemic and animal disease period (2023 - 2025). Moreover, most of the research ignores an important shift in the hog market structure: the formation of an oligopolistic market due to the elimination of small-scale producers during the ASF. 

The novelty of this essay is that it offers a micro-level explanation of a broad macroeconomics topic. It argues that the strategic decisions made by the dominant firms in the hog market have not only undermined the effectiveness of the policy, but also contradict the policy’s intent. This paper also explains that the “National Pork Reserve” mechanism has unintentionally created a moral hazard. By reducing the firms’ risk of profitability, the policy incentivizes them to expand aggressively, leading to even more volatile price fluctuation. In response, this research asks: **To what extent has the “National Pork Reserve” been effective in reducing price volatility in the Chinese hog market, given the counter-cyclical production strategies of oligopolistic suppliers between 2023 and 2025?**

## 2. Methodology
This essay will combine both quantitative analysis and theoretical reasoning to assess the “National Pork Reserve” mechanism in stabilizing the hog price between 2023 to 2025. 

To measure the market supply, this research uses the “breeding sow inventory” instead of current slaughter volume. This is because the sow inventory serves as the fundamental capital for hog production. The slaughter volume only indicates the production decisions made 10 months ago (a breeding period), whereas the sow inventory reflects the producers’ current decision on future production level. 

The analysis uses a variety of data sources: secondary data collected from official government websites, credible academic research and market insight websites. No primary data are used because, to analyze price volatility, an aggregate market outcome, large volumes of secondary data is preferred over primary data which is often limited in size.

The quantitative analysis uses the Interrupted Time Series (ITS) model — “a quasi-experimental method for evaluating interventions by observing trends before and after an intervention” (Gregorich, 2016). 

This is formulated as:

$$Price_t = \beta_0 + \beta_1(Time_t) + \beta_2(Policy_t) + \beta_3(TimeAfterPolicy_t) + \epsilon_t$$

This is a comparison of the trend in hog price before and after intervention by identifying a point of structural discontinuity. Therefore, a specific date of structural shift is required. In this investigation, the date chosen is 2024/05/09. While numerous interventions (e.g., 2023/07/12, 2023/12/25) had been implemented before, they were merely routine purchases to temporarily support price level, the fundamental market structure remained unchanged. In contrast, the May 2024 intervention represents a long-term supply-side structural reform. Because in March 2024, the NDRC announced a change in target of the “National Pork Reserve” mechanism — a reduction in target sow inventory production volume from 41 to 39 million. As economic policies often have a time lag to observe real impact, the 2 month gap between March and May accounts for this, ensuring that the observed trend reflects firms’ behaviors adjusted to the altered policy.  

Calculations of the coefficients are done using Python.

The ITS model fails to consider external factors such as producers’ cost of production. Consequently, the ITS model will only be used to provide empirical evidence of price volatility, which complements the theoretical analysis. 

## 3. Theoretical Framework & Policy Mechanism

### 3.1 Cobweb Theorem
The cobweb model helps to explain the hog price fluctuation cycle. It assumes that producers have “adaptive expectations”. It argues that in a market of agricultural goods, in this case, hog, producers determine the future production level ($Q_{t+1}$) based on current price level ($P_t$). Hogs take approximately 10 months to reach the conditions for sell, when $Q_{t+1}$ amount of hog is ready for sell, the price changed from $P_t$ to $P_{t+1}$, leading to a change in quantity demanded. As the short run supply is perfectly inelastic, a mismatch between quantity supplied and quantity demanded is created, resulting in a disequilibrium (Harlow, 1960).

The cobweb theorem claims that, if the price elasticity of supply (PES) is greater than the price elasticity of demand (PED), the price volatility would follow a divergent trend, signifying that price volatility will amplify over time rather than self-correct. For example, in figure 1, an initial supply side shock results in an increased price from P0 to P1, therefore signalling the producers to expand production from Q0 to Q2. However, when the quantity supplied increased to Q2, the price crashed to P2, resulting in an excess demand of Q2-Q3. Producers then start to aggressively decrease the production level until it reaches Q3, where price is driven up again due to the rare supply. A divergent cyclical trend is observed (Dean, 1958).

*[Insert Figure 1: Divergent Cobweb Model here]*

The divergent model can be applied to the Chinese hog market as pork approximately occupies 60% of the meat consumption in China, indicating an inelastic consumer PED. The increased market domination of large-scale hog producers means that producers can adjust their output easily, leading to an elastic PES. 

However, the cobweb model has limitations as producers may not be as short-sighted as the model assumes. In reality, while true for small-scale producers, mega-producers such as Muyuan Food rely on sophisticated big data and live hog future markets to make production decisions. 

### 3.2 Theoretical Policy Effects
To artificially correct the divergent Cobweb behavior in the hog market, the Chinese government implemented the “National Pork Reserve” mechanism.

The Pig - Grain price ratio is used to gauge the hog producers’ profitability, as grain is the main ingredient to feed pigs. The Pig - Grain ratio is a complex index which depends on two variables: Hog price and Grain price. Theoretically, the index could fall below the boundary level with a substantial increase in price of grain but a constant hog price. However, the grain price has a slow, linear decline during the observed period (2023 - 2025), whereas hog price shows a high amplitude volatility. Therefore, statistically, the aggressive fluctuation in the Pig - Grain price ratio in this study is mainly driven by the hog market, not the grain market. 

The mechanism functions differently in 2 scenarios. 

#### 3.2.1 Scenario A: Price Floor Interventions During Oversupply
The first scenario is when the Pig - Grain ratio falls below 5:1, in which producers start to make losses. 

Short term supply of hog is perfectly inelastic ($S_{fixed}$) due to the biological lag of hog production, the quantity (Q0) cannot be reduced instantaneously. P0 is the equilibrium price determined by the intersection of the demand D and supply $S_{fixed}$ curves, with the corresponding equilibrium quantity Q0. However, the government’s target price is $P_{target}$, with quantity at Q1. The initial price is lower than the government target price, which produces an oversupply of Q0 - Q1. 

In order to drive the price up, the government activates the “National Pork Reserve” mechanism by purchasing the excess supply (Q0 - Q1) to artificially drive the market into a new equilibrium.

*[Insert Figure 2: Price Floor Interventions During Oversupply here]*

As a result, the intervention absorbs the excess supply and mechanically drives the price up from P0 to $P_{target}$. This prevents the price from continuing crashing and therefore stabilizes the hog price.

#### 3.2.2 Scenario B Price Ceiling Interventions During Shortages
The second scenario is when the Pig - Grain ratio exceeds 12:1, which indicates a substantial increase in hog price. 

Comparing to scenario A, in this case, the initial price and quantity is higher than the government target price level ($P_{target}$), and quantity (Q1). As a result, a shortage is produced. 

The “National Pork Reserve” mechanism operates differently to combat the high price, it directly injects hog supply into the market to mitigate the supply shortage (Q1 - Q0), shown by the rightward shift of supply curve in Figure 3a. 

*[Insert Figure 3: Price Ceiling Interventions During Shortages here]*

## 4. Quantitative Analysis: Interrupted Time Series (ITS) Modeling

### 4.1 Regression Results
Figure 4 shows the weekly hog price during the observed period (2023-2025). The ITS model builds analysis based on this raw data. 

*[Insert Figure 4: Weekly Hog Price (2023-2025) here]*

The intervention date chosen is 2024/5/9, on which date, the Pig - Grain ratio stood approximately at 6.2:1 (calculated by hog price/corn price: 15.16/2.45), which is technically higher than the 5:1 intervention activation ratio. Although the condition is not fulfilled, the decision to implement a structural supply-side shift — lowering the target sow inventory from 41 million to 39 million; was due to the persistent price stagnation.

In Figure 4, during the pre-intervention (January 2023 - May 2024), the hog price remained trapped in a long-run low level, despite multiple “National Pork Reserve” purchases to support the low average price level, it shows a decreasing trend to breach the breakeven point. This demonstrates that standard supply purchases were insufficient to combat the overcapacity caused by the continuous expansion of oligopolies. 

To quantify the impacts of this structural shift, the ITS model is applied. The numerical value of the coefficients are shown in Table 1. 

**Table 1: OLS Regression Results (ITS)**

| Variable | Coef. | Std. Err. | t-value | P-value |
| :--- | :--- | :--- | :--- | :--- |
| **Intercept ($\beta_0$)** | 15.4638 | 0.2291 | 67.5053 | 0.0000 |
| **Time Trend ($\beta_1$)** | -0.0006 | 0.0008 | -0.7095 | 0.4791 |
| **Level Change ($\beta_2$)** | 4.3567 | 0.3144 | 13.8561 | 0.0000 |
| **Slope Change ($\beta_3$)** | -0.0114 | 0.0010 | -11.1804 | 0.0000 |

* **R-squared:** 0.7299
* **Adj. R-squared:** 0.7243
* **Obs.:** 151
* **F-statistic:** 132.38

Price volatility is measured by the standard deviation of the hog prices in pre-intervention and post-intervention period. 

* **Pre-intervention:** 0.8708
* **Post-intervention:** 2.3684

The “National Pork Reserve” mechanism failed to stabilize the hog price and amplified price fluctuations instead. This does not mean that the theoretical policy effect is misinterpreted, the failure is mainly caused by the large-scale producers’ strategic behaviors (explained in section 5). 

In summary the model used highly fits the study, with an adjusted R-squared of 0.7243, which indicates that the variables chosen explain approximately 72.4% of the hog price variance. 

### 4.2 Coefficient Interpretations
The coefficient $\beta_1$ has a value of -0.0006, indicating that the trend of hog price was somewhat decreasing in the pre-intervention period. However, a P-value of 0.4791 means that the value is statistically insignificant, as 0.4791 > 0.05. Which supports the previously made point of the price stagnation in the pre-intervention period, as the market had no significant trend and the hog price was trapped between 14 - 17 CNY/kg. 

#### 4.2.1 Phase 1: Speculative Bubble
$\beta_2$ measures the immediate effect on the hog price due to the intervention. It holds a value of 4.3567, which is positive and statistically significant (P-value < 0.05). This demonstrates that the immediate effect of the supply-side reform was a sharp increase in hog price — the intervention successfully boosted the previously low hog price. However, data on sow inventory reveals that this spike in hog price was not due to actual physical reduction in amount supplied, but rather market expectations. 

When the government announced the reduction in target sow inventory, the producers expected a shortage in the market, they therefore aggressively purchased hogs to avoid a higher price in the future. This increased demand for hogs (Xiong, 2024). The official data from the Ministry of Agriculture and Rural Affairs shows that the national breeding sow inventory was 39.86 million in April 2024. When the price started to show an increasing trend, producers ignored the 39 million target sow inventory and expanded supply to 40.38 million by June in the same year.

However, the consistent price increase from 15.16 ￥/kg on May 2024 to a peak of 20.92 ￥/kg on September 2024 was a substantial increase of 38% which lasted 3 months. The demand driven by future price expectations is unlikely to last for 3 months, there must be supply-side factors that contribute to this drastic increase. 

To identify the supply-side factors, it is necessary to recognize the oligopolistic feature of the Chinese hog market. As mentioned in the introduction, the previous Chinese hog market full of small-scale producers has changed completely due to the African Swine Fever between 2018 and 2022, where a massive amount of small-scale producers were forced into bankruptcy. As a result, large-scale producers such as Muyuan Food and Wens consolidated the market quickly. This can be quantified by the market concentration ratio of the top 10 hog producers, which increased from under 10% in 2018 to approximately 23% in 2023. This transformation of market structure granted the dominant firms strong pricing power and the ability to influence supply-side of the market through their strategic decisions.

As a result, the dominant firms in the hog market engaged in “withholding of slaughter” and “secondary fattening” — ideas introduced by Kephart et al., 2005. The ideas refer to livestock producers’ strategy of holding the hogs with standard weight for a longer period of time in order to feed them to a heavier weight, rather than supplying them immediately into the market, artificially creating a shortage in the market, forcing the price up. This action is incentivized in this case by the expectation of higher future prices in the hope of a higher profit. Empirical evidence exists to support this idea, MARA shows in its report that the national average slaughter weight increased from 121.5 kg in April 2024 to 125.5 kg in September 2024. Moreover, an industrial report indicates that the price gap between hogs with normal weight and hogs with weight over 150 kg has widened significantly during the same time period, which further encourages withholding of slaughter and secondary fattening (Li, 2025). 

*[Insert Figure 5: Profit Maximization by Secondary Fattening here]*

The shortage ($Q_{restricted}$) shown in Figure 5 can also be proven by data from MARA. In June 2024, the monthly slaughter volume was 24.31 million head, a 8.8% decrease from the previous month to the start of the intervention. This unusual decrease in the slaughter volume reinforces the idea that the shortage was not caused by natural market equilibrium change, instead, by artificial forces that drove the price up to $P_{max}$.

This speculative bubble builds foundation for the drastic decrease in price in phase 2 (September 2024 to September 2025). Producers cannot withhold these heavy hogs for an indefinite time, therefore, when they expect a decreasing price trend, they will liquidate these inventories (Yang, 2023). This happened in November 2024, when the price had been consistently falling from its peak in September 2024. According to statistics provided by MARA, in November 2024, the monthly slaughter volume exploded to 41.62 million head, an approximately 30.5% increase from the previous month. The result was that the market was shocked by this massive amount of supply, it broke the price bubble and the market price from then showed a consistent decreasing trend. In this study, this period of consistent decreasing price is called phase 2.

#### 4.2.2 Phase 2: Inventory Liquidation and the Structural Crash
$\beta_3$ measures the difference between the slope of price regressions before and after intervention. It holds a negative value of -0.0114, which is statistically significant (P-value < 0.05) and indicates an accelerated downward trend compared to the pre-intervention period, this can be visualized by the red line’s steeper slope. The continuous fall in price is due to the break of the speculative bubble. 

## 5. Qualitative Analysis: A Game Theoretical Model of Oligopolistic Moral Hazard
In this section, Muyuan food is selected as the representative firm to the dominant firms’ behavior in the market, as it is the largest hog producer that controls approximately 10% of the slaughter volume in the Chinese hog market. 

The aggressive nature of the phase 2 price crash cannot be explained by the traditional model of perfect competition, where firms are signaled to cut production when price falls below the break-even point. If firms behave the same way, the hog price would eventually stabilize at a new equilibrium point. 

However, the market's self-correction mechanism assumes that no external interventions and market power are involved in the market. This is not true in this case, as the Chinese hog market is oligopolistic, where dominant firms make decisions not only based on the price, but also the competitors’ decisions and the overall market environment. More specifically, the “National Pork Reserve” mechanism heavily influences the dominant firms’ long-term strategic decisions — making them reluctant to cut production. This investigation uses game theoretical models to explain this phenomenon. 

### 5.1 Moral Hazard
Moral hazard refers to the action of increasing one’s exposure to risks when the one bears the minimum of the cost. In the context of the Chinese hog market, the “National Pork Reserve” mechanism serves as an insurance to the producers. This is because the government will purchase the excess supply when the producer’s profitability is low enough, which means that the government unintentionally absorbs the financial consequences of overproduction (Rao, 2019). 

Empirical evidence also supports this argument, during phase 2, the dominant firms kept the sow inventory above 40 million heads despite the decreasing price. As a result, in August 2025, when the price falls below the intervention triggering level (14.3 ￥/kg), the NDRC conducted a purchase of 10000 ton of frozen pork to bail the firms out. This round of purchase directly granted Muyuan Food 96.31 million RMB according to the company’s 2025 3rd quarter financial report. 

However, the revenue gained is so small that it only constitutes roughly 1% of Muyuan Food’s total revenue in 2025. So why did the firms keep expanding?

To answer this question, it is essential to understand that in an oligopolistic market, dominant firms mainly try to gain long-term market share rather than short-term profit maximization (Stuart, 2014). While the revenue gained from state purchase is relatively small, its main purpose is risk reduction rather than profit generation. The 1% is essential as it could compensate dominant firms’ fixed costs to prevent these firms from going bankrupt. 

Thanks to the moral hazard created by the mechanism, the dominant firms can now engage in supply expansion to keep the price low enough to be able to eliminate small firms out of the market and therefore gain more market share. 

This essay mainly focuses on supply-side factors that result in the prolonged price stagnation in phase 2, however, demand-side factors such as consumer disposable income and changing consumer preference have not been considered, which is one of the limitations of the analysis. 

### 5.2 Prisoner’s Dilemma
While aggressive supply expansion is the logical strategy for a single firm in the hog market, the reality is that almost all the mega-firms are applying the same strategy simultaneously. According to the top 20 firms’ financial report in 2025, Muyuan Food dumped an astonishing 78 million hogs into the market in the single year of 2025, with an increase of 6.4 million head from the previous year. Moreover, Wens Foodstuff, the second largest hog supplier in the market, increased its production by 10.3 million hogs from 2024 to 2025. 

As all the dominant firms aim for the spare market share left by the bankrupting small-scale producers, their strategic decisions altered the risk-reward calculus in the market, resulting in a classic game of Prisoner’s Dilemma.

Firms’ payoff matrix is shown in the following payoff matrix.

**Oligopolies Payoff Matrix**

| | Firm B: Cut | Firm B: Expand |
| :--- | :--- | :--- |
| **Firm A: Cut** | (5, 5) | (-2, 10) |
| **Firm A: Expand** | (10, -2) | (-1, -1) |

The payoffs inside the payoff matrix do not represent any real world value, they are symbolic values indicating the utility of the given strategy chosen by firms. 

When both firms choose to contract supply, they gain a mutual benefit of (5, 5). This means that the firms would gain a moderate but stable profit as the hog price would then be stabilized in an equilibrium price exactly as the effect mentioned in the Theoretical Policy Effect section. 

However, when one firm expands and the other contracts, it results in a highly asymmetrical payoff of (10, -2) or (-2, 10). The one that expands production in this case would gain massive benefit by obtaining an enormous amount of market share and therefore gain long-term competitive advantage. This reward is extremely attractive to firms in an oligopoly as it offers them a chance to monopolize the market. 

In the last scenario, both firms choose to expand production, and achieve a payoff of (-1, -1), which is the Nash equilibrium of this game. This is because every firm has a dominant strategy of expansion (10) and they would not risk the devastating loss of market share (-2), none of them can increase their own payoff by unilaterally changing their strategy. This signifies that the supply would keep increasing and therefore drive the price down consistently, as shown by the negative trend of price in phase 2. 

In a free market, this game will come to an end when the price is low enough to cause mutual financial insolvency (-10, -10), where the firms are forced to liquidate all the inventories and therefore create a new equilibrium.

However, as mentioned in 5.1, the “National Pork Reserve” policy creates a moral hazard which distorts the market self-correction. By artificially providing an insurance that caps the oligopoly’s worst payoffs at Nash equilibrium to (-1, -1), the government reduces the risk of firms going bankrupt in such aggressive competitions. As a result, firms are willing to stay at that Nash equilibrium to slowly absorb market share from failing small firms. According to the year-end industry report for 2025, the market share of small firms shrank to below 30% and the top-20 hog producers’ market concentration rate reached nearly 30% (boyan, 2025). 

This Prisoner’s Dilemma analysis relies on the firms to make rational choices, which is not always true in reality as multiple external factors such as different business objectives could result in distinct strategic decisions. 

It is also acknowledged that there are far more firms involved in this strategic interaction, however, the logic is the same, no matter how many players are added to the game, as long as the ordinal payoff structure remains consistent, the Nash equilibrium will not change. 

## 6. Conclusion
In conclusion, this essay finds that the “National Pork Reserve” mechanism implemented by the Chinese government failed to stabilize the cyclical price volatility in the local hog market, which can be statistically proven by the substantially increased standard deviation (from 0.8708 pre-intervention to 2.3684 post-intervention) and the accelerate downward price trend ($\beta_3$ = -0.0114) captured by the ITS model. This investigation also discovers that the failure is not due to a mathematical flaw in the policy itself, instead, it occurred as the policy provides an insurance to the newly formed oligopolies which allows them to ignore short-term profit and conduct a predatory strategy of expansion, in order to eliminate small-scale producers and therefore increase market dominance. 

By illustrating the strategic interactions between dominant firms in the market, this essay shows that the predatory expansion locked the industry into a Prisoner’s Dilemma with a single Nash equilibrium at (expand, expand), which explains logically why almost all the dominant firms involved in supply expansion in 2025.

Nevertheless, definitive claims are limited by the ITS model’s inability to account for sudden biological factors such as swine fever, although a period without major livestock diseases is chosen, livestock’s health condition is still crucial to be taken into consideration as it has the potential to affect price significantly. 

Regardless of these limitations, an extensive empirical study clearly demonstrates the unintended consequences caused by this policy. Considering the increasing market consolidation by the large-scale producers, the Chinese government must change its policy direction — rather than solely focus on macroeconomic intervention that affect demand and supply, future policies must consider microeconomic regulations to limit oligopolies’ market power and restructure the current mechanism to avoid creating moral hazard. 

## 7. Bibliography
[Insert Bibliography Here]

## 8. Appendix
[Insert Appendix Here]
