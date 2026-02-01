<h1>To what extent do changes in net migration explain variations in median house prices across Australia's states and territories?</h1>

<h2>Overview</h2>
This project examines the relationship between <strong>net overseas migration</strong> and
<strong>median house prices</strong> across Australia's states and territories.
<ul style="list-style-type: square">
    <li>Using housing, population, and migration data from the Australian Bureau of Statistics (ABS),
    the analysis explores whether changes in net migration are associated with variations in median
    house prices over time.</li>
    <li>The results aim to <strong>contribute to policy discussions on housing
    affordability and population growth</strong> by clarifying the extent to which migration alone explains
    housing price variation, and by highlighting the importance of additional structural and
    economic factors.</li>
</ul>
<h2>Objectives</h2>
<ol class="body-text">
<li>Identify and assess the availability and structure of relevant housing, population, and migration data.</li>
<li>Calculate net migration rates and median house prices for each Australian state and territory.</li>
<li>Examine temporal trends and explain notable variations by reference to major real-world events, such as the COVID-19 pandemic.</li>
<li>Visualise the relationship between net migration and median house prices across states and territories.</li>
<li>Quantify the statistical correlation between net migration rates and changes in median house prices using Pearson's correlation and corresponding hypothesis tests.</li>
</ol>
<h2>Hypotheses</h2>
<ul class="body-text">
<li><strong>Null hypothesis (H<sub>0</sub>):</strong> There is no statistically significant linear relationship between net overseas migration rates and changes in median house prices across Australia's states and territories.</li>
<li><strong>Alternative hypothesis (H<sub>1</sub>):</strong> There is a statistically significant linear relationship between net overseas migration rates and changes in median house prices across Australia's states and territories.</li>
</ul>
<h2>Data and Methodology</h2>
<h4>Interpretation and Scope</h4>
<ul class="body-text" style="list-style-type: square">
<li>This analysis focuses on identifying associations between migration
and median house prices.</li>
<li>While the observed relationships are economically intuitive,
<strong>the results should not be interpreted as causal effects</strong>.</li>
<li>Potential confounding factors include interest rates, zoning regulations, credit
conditions, and local economic shocks. </li>
<li>As such, findings are best interpreted as
descriptive and explanatory rather than causal.</li>
</ul>
<h4>Datasets Used (Source: Australian Bureau of Statistics)</h4>
<ul class="body-text" style="list-style-type: square">
<li>Net Overseas Migration</li>
<li>Estimated Resident Population (States and Territories)</li>
<li>Median Price and Number of Transfers (Capital City and Rest of State)</li>
</ul>

<strong class="body-text">All data cleaning and relevant preprocessing steps were conducted in a separate notebook for the datasets that required it. This notebook focuses on exploratory data analysis and analysing correlations using statistical techniques.</strong>
<h4>Data Preparation Summary</h4>
<ul class="body-text" style="list-style-type: square">
<li>Filtered data to remove header cells that contained metadata</li>
<li>Removed all columns that did not contain data</li>
<li>Changed the indices and columns of the datasets to what is required for our analysis.</li>
</ul>
<h4>Justification of data sources</h4>
<ul class="body-text" style="list-style-type: square">
<li>The analysis was conducted at the state level using annual data.</li>
<li>Annual migration data was used to reflect the slow-moving and policy-driven nature
of migration decisions, as well as the delayed response of housing prices
due to planning constraints and construction timelines. </li>
<li>Using annual data reduces short-term volatility and allows the analysis to focus on
structural relationships rather than transitory fluctuations which are commonly seen in quarter-frequency migration data.</li>
<li>We used pricing data that came along with number of transfers of each residential building type to allow more accurate estimation of the median house prices for each state, and by extension, the median price across all of Australia.</li>
</ul>

<h2>Summary of our findings</h2>
<ul class="body-text" style="list-style-type: square">
<li><h4>Consistency with reality</h4>
<ul style="list-style-type: square">
<li>Our data across all states was generally consistent with the behaviour of house prices and migration over the past 18 years.</li>
<li>The data exhibited expected spikes and drops during notable events such as the COVID-19 pandemic where migration was at record lows in 2020 but began to spike considerably in 2022-2023.</li>
<li><strong>Outliers in migration rates</strong>, both extreme highs and extreme lows, were seen around time period of the COVID-19 pandemic where many states such as New South Wales and Victoria experienced extreme surges in migration after lockdown had ended and record lows (or losses) in net migration during the pandemic lockdown itself.</li>
</ul>
</li>
<li><h4>Correlation findings</h4></li>
<ul class="body-text">
<li>At a <strong>national level</strong>, the correlation between house prices and migration rates was seen to be <strong>weak</strong> as indicated by the p value $p=0.298$ which leads us to not reject the null hypothesis.</li>
<li>The overall correlation between net migration per 1000 residents and % change in median house prices was <strong>weak</strong> across <strong>all states</strong>, as evident by the scatter plots and the p values for each state which imply that there is insufficient evidence to reject the null hypothesis.</li>
<li>However, the <strong>Australian Capital Territory</strong> was an exception where there was strong statistical evidence found to believe there was a linear relationship between net migration and change in house prices in the state. The linear correlation was found to be <strong>negative and relatively strong</strong>, indicated by the Pearson correlation $-0.683$.</li>
</ul>
<li><h4>Limitations of the analysis</h4></li>
<ul class="body-text">
<li><strong>Availability of residential building types:</strong> Data for median house prices were only available for detached dwellings and established houses.</li>
<li><strong>Availability of migration data on a city level:</strong> Having access to migration rates within cities provides more data points with which we can analyse the correlation between migration rates and house price changes.</li>
<li><strong>Lack of a wider reference period:</strong> Having access to migration data that goes back earlier than 2006 (like our housing price data which goes as far back as 1983) would provide more data points to use in our correlation analysis.</li>
</ul>
<li><h4>Potential improvements</h4></li>
<ul class="body-text">
<li><strong>Incorporating other major factors such as interest rates</strong> would provide a clearer picture of the drivers of housing prices in Australia, which would allow the government to make more informed decisions on how to tackle one of nation's biggest issues.</li>
<li><strong>Investigating the possibility</strong> that housing prices and migration rates may follow a <strong>non-linear</strong> relationship and thus, explore whether a different kind of relationship is possible.</li>
<li>Gaining access to migration data spanning a wider reference period would provide more data points for the correlation analysis, making our conclusions more reliable and indicative of how house prices and migration rates behave together.</li>
</ul>
</ul>
