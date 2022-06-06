# DatabookRepo

## Introduction 
Hi! Welcome to my day-to-day dataset. <br/> I have been work a lot with numbers on the enviroment, the economy and production, and maybe it can help you all.
Sources, code lines and final datasets are available. All data description is listed below. Mostly done in R. <br/>

All data is divided into four 5 categories: Default Patterns, Greenhouse Gases (GHGs) Emissions, Land-Use and Farming, World Indicators and Brazilian Indicators. 
Dates are always set on YYYY-MM-DD format (if available).

Tips and comments are totally welcome!
For some dataviz-related work, follow me on Twitter: [@hec_vini](https://twitter.com/hec_vini). Also, connect with me on [LinkedIn](https://www.linkedin.com/in/viniciushpires/)

## Introduction
Welcome to my data repository. For the lasts mosnths, I have been working a lot with exploratory data analysis on the Brazilian reality (socioeconomical and enviromental), coutries profilies and greenhouses gases emissions. Although every data available here is public, I hope I can help you by displaying it on a clean and more organized format. Also, I have prepared a







1.
# Default Patterns

This section contains data used all over the dataset, like inflation indexes and geographic regionalization.

1. Inflation

**IPCA** : Brazilian main Consumer Price Index (CPI). Inflation index for household incomes between 1 and 40 minimum wages (aprox. BRL 1200 to 48000, in 2022). For full methodology, check out [IBGE&#39;s](https://www.ibge.gov.br/estatisticas/economicas/precos-e-custos/9256-indice-nacional-de-precos-ao-consumidor-amplo.html?=&amp;t=conceitos-e-metodos) page.

Source: IBGE

Coverage: 1996/01/01 – 2020/12/01

Columns Description:

_ **date** _ _(\&lt;date\&gt;): date format in YYYY-MM-DD._

_ **inflation\_index** _ _(\&lt;dbl\&gt;): inflation index for each month. Dec 1993 = 100._

**IPCA Monthly** : monthly change on IPCA index.

Source: IBGE

Coverage: 1996/01/01 – 2020/12/01

Columns Description:

_ **date** _ _(\&lt;date\&gt;): date format in YYYY-MM-DD._

_ **cumulative\_inflation** _ _(\&lt;dbl\&gt;): cumulative inflation, in Jan 2021, for each month._

**IPCA Yearly** : yearly change on IPCA index.

Source: IBGE

Coverage: 1996 – 2020

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year_

_ **cumulative\_inflation** _ _(\&lt;dbl\&gt;): cumulative inflation, in Dec 2020, for each year. Changes on inflation index between each December index._

**Brazilian GDP Implicit Deflator** : Brazilian price changes, measured on changes in Brazilian GDP real price changes. For more information, check out this [BLS](https://www.bls.gov/opub/mlr/2016/article/comparing-the-cpi-with-the-gdp-price-index-and-gdp-implicit-price-deflator.htm) report.

Source: IBGE

Coverage: 1999 – 2020

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year_

_ **cumulative\_inflation** _ _(\&lt;dbl\&gt;): cumulative inflation, in Dec 2020, for each year. Changes on inflation index between each December index._

1. Brazilian Geographical Regions

**Municipalities Codes** : Brazilian cities IBGE regionalization. Useful to deal with city-level data. For a full list of IBGE&#39;s surveys on cities indicators, check out [IBGE Cidades](https://cidades.ibge.gov.br/) website.

Source: [IBGE](https://www.ibge.gov.br/geociencias/organizacao-do-territorio/estrutura-territorial/23701-divisao-territorial-brasileira.html?=&amp;t=acesso-ao-produto)

Coverage: all 5570 Brazilian cities, in 2022

Columns Description:

_ **id\_municipality** _ _(\&lt;dbl\&gt;): 7-number city code_

_ **name\_municipality** _ _(\&lt;chr\&gt;): cities names, as on IBGE&#39;s dataset. For some cities, spelling may change according to the source (e.g., Eldorado dos Carajás vs. Eldorado do Carajás). Prefer using municipalities ID&#39;s rather than its names&#39;._

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state (in Portuguese: &quot;Unidade da Federação&quot;) code_
_ **name\_state** _ _(\&lt;chr\&gt;): states names_

_ **code\_state** _ _(\&lt;chr\&gt;): states 2-letter abbreviation_

**States Codes** : list of Brazilian states codes.

Source: [IBGE](https://www.ibge.gov.br/geociencias/organizacao-do-territorio/estrutura-territorial/23701-divisao-territorial-brasileira.html?=&amp;t=acesso-ao-produto)

Coverage: all 26 states + 1 Distrito Federal, in 2022.

Columns Description:

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number states codes (in Portuguese: &quot;Unidade da Federação&quot;). 1 = Brasil._

_ **code\_state** _ _(\&lt;chr\&gt;): states 2-letter abbreviation. 1 = BR_

**Immediate Regions Codes** : list of Brazilian immediate regions. Immediate regions are groupings of municipalities, by economic, political and environmental common characteristics, according to IBGE&#39;s methodology. It may be useful to deal with city level data, due to the reduction of outlier data.

Source: [IBGE](https://www.ibge.gov.br/geociencias/organizacao-do-territorio/estrutura-territorial/23701-divisao-territorial-brasileira.html?=&amp;t=acesso-ao-produto)

Coverage: all 510 immediate regions, in 2022.

Columns Description:

_ **id\_immediate\_region** _ _(\&lt;dbl\&gt;): 6-number immediate region code._

_ **name\_immediate\_region** _ _(\&lt;chr\&gt;): immediate regions names, as on IBGE&#39;s dataset._

_ **id\_municipality** _ _(\&lt;dbl\&gt;): 7-number city code._

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number states codes (in Portuguese: &quot;Unidade da Federação&quot;)._

**Microregions Codes** : list of Brazilian microregions. IBGE&#39;s antecessor to immediate regions. Some datasets still use this regionalization format.

Source: [IBGE](https://www.ibge.gov.br/geociencias/organizacao-do-territorio/divisao-regional/15778-divisoes-regionais-do-brasil.html?=&amp;t=acesso-ao-produto)

Coverage: all 558 microregions, in 2022.

Columns Description:

_ **id\_microregion** _ _(\&lt;dbl\&gt;): 5-number microregion code._

_ **name\_microregion** _ _(\&lt;chr\&gt;): microregions names, as on IBGE&#39;s dataset._

_ **id\_municipality** _ _(\&lt;dbl\&gt;): 7-number city code._

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number states codes (in Portuguese: &quot;Unidade da Federação&quot;)._

**Municipalities Codes (6n)**: 6-number and 7-number Brazilian municipalities codes. The first pattern is not the default one, but it is still used in some dataframes.

Source: [IBGE](https://www.ibge.gov.br/geociencias/organizacao-do-territorio/estrutura-territorial/23701-divisao-territorial-brasileira.html?=&amp;t=acesso-ao-produto)

Coverage: all 5570 Brazilian cities, in 2022

Columns Description:

_ **id\_municipality** _ _(\&lt;dbl\&gt;): 7-number city code._

_ **id\_municipality\_6n** _ _(\&lt;dbl\&gt;): 6-number city code._

**Municipalities Biomes** : list of Brazilian cities, according to the biome that it is part of. Brazil has six distinct biomes: &quot;Amazônia&quot;, &quot;Cerrado&quot;, &quot;Pantanal&quot;, &quot;Caatinga&quot;, &quot;Mata Atlântica&quot;, and &quot;Pampa&quot;.

Source: [IBGE](https://www.ibge.gov.br/geociencias/cartas-e-mapas/informacoes-ambientais/15842-biomas.html?=&amp;t=acesso-ao-produto)

Coverage: all 5570 Brazilian cities, in 2022.

Columns Description:

_ **id\_municipality** _ _(\&lt;dbl\&gt;): 7-number city code._

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number states codes (in Portuguese: &quot;Unidade da Federação&quot;)._

_ **biome** _ _(\&lt;chr\&gt;): municipality biome. No city has more than one biome, according to IBGE&#39;s methodology._

1. World Regionalization

**ISO-3c UE27:** list of EU27 countries ISO-3c codes. Displayed on list format.

Source: [EU](https://european-union.europa.eu/principles-countries-history/country-profiles_en)

Coverage: EU27 countries. Does not include the UK, Switzerland, Norway, Iceland, and Liechtenstein.

**World Bank Income** : list of countries, according to its income level. Each country may be considered &quot;high income&quot;, &quot;upper middle income&quot;, &quot;lower middle income&quot; and &quot;low income&quot;. In 2021 methodology, countries with GNI higher than USD 12 695 were considered as &quot;high income&quot;.

Source: [The World Bank](https://blogs.worldbank.org/opendata/new-world-bank-country-classifications-income-level-2021-2022)

Coverage: 217 countries.

Columns Description:

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code._

_ **region** _ _(\&lt;chr\&gt;): each country region, according to the 7 regions set by the World Bank.
# 1_

_ **income\_group** _ _(\&lt;chr\&gt;): each country World Bank income group._

1.
# GHGs Emissions and Carbon Pricing


1. Climate Watch (CAIT/WRI)

 CAIT GHGs data is one of the most used emissions databases. It comprehends sectoral CO2e for 193 countries, over 1990 – 2018 period. It used IPCC&#39;s AR4 100-year GWP conversion factors and account for LULUCF emissions. Original economic activity data mainly come from FAO, IEA, the Global Carbon Project (GCP) and the US EPA. It does not use countries official carbon emissions repositories.
 CAIT&#39;s data is useful to compare country-to-country emissions, although it may not be useful if granularity is the desirable characteristic.


**CAIT** : wide to long transformation of CAIT&#39;s data.

Source: [CAIT/WRI](https://www.climatewatchdata.org/ghg-emissions?end_year=2019&amp;start_year=1990). For full methodology prospects, check out this [document](https://www.climatewatchdata.org/about/faq/ghg).

Coverage: 193 countries on the 1990 – 2018 period, for 14 sectors.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code. Does not include EU27 (&quot;EUR&quot;), World (&quot;WLD&quot;) emissions and international emissions._

_ **sector** _ _(\&lt;chr\&gt;): emission sector. Mind that there are overlapping emissions on &quot;Total&quot; and &quot;Energy&quot; categories._

_ **emissions** _ _(\&lt;chr\&gt;): yearly emissions, by sector. In millions of tons of CO __2__ e._

_ **unit** _ _(\&lt;chr\&gt;): unit of emissions data. In this dataset, all numbers are expressed in terms of Mt of CO __2__ e._

**CAIT (All Sectors)**: wide to long transformation of CAIT&#39;s data. Instead of each country emissions profile, EU27 emissions are under &quot;EUR&quot; ISO3c.

Source: [CAIT/WRI](https://www.climatewatchdata.org/ghg-emissions?end_year=2019&amp;start_year=1990).

Coverage: 166 countries + EU27, on the 1990 – 2018 period. 14 sectors, including totals.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code. It includes EU27 (&quot;EUR&quot;) and does not include EU countries own emissions, neither World (&quot;WLD&quot;) emissions._

_ **sector** _ _(\&lt;chr\&gt;): emission sector. Mind that there are overlapping emissions on &quot;Total&quot; and &quot;Energy&quot; categories._

_ **emissions** _ _(\&lt;chr\&gt;): yearly emissions, by sector. In millions of tons of CO __2__ e._

_ **unit** _ _(\&lt;chr\&gt;): unit of emissions data. In this dataset, all numbers are expressed in terms of Mt of CO __2__ e._

**CAIT (Main Sectors)**: wide to long transformation of CAIT&#39;s data. Sectoral data was organized to exclude overlapping data. Here, emissions are organized in 5 categories: &#39;Agriculture&#39;, &#39;Energy&#39;,&#39; Land-Use Change and Forestry&#39;, &#39;Waste&#39;, &#39;Industrial Processes&#39;. Mind that energy emissions in composed, mainly, from electricity production, heating and transportations. For Energy detailing, please, use CAIT (All Sectors) dataset.

Source: [CAIT/WRI](https://www.climatewatchdata.org/ghg-emissions?end_year=2019&amp;start_year=1990).

Coverage: 166 countries + EU27, on the 1990 – 2018 period, for 5 sectors. Energy emissions are not detailed.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code. It includes EU27 (&quot;EUR&quot;) and does not include EU countries own emissions, neither World (&quot;WLD&quot;) emissions._

_ **sector** _ _(\&lt;chr\&gt;): sectoral emissions data, organized in 5 categories: &#39;Agriculture&#39;, &#39;Energy&#39;,&#39; Land-Use Change and Forestry&#39;, &#39;Waste&#39;, &#39;Industrial Processes&#39;. Mind that energy emissions in composed, mainly, from electricity production, heating and transportations. For Energy detailing, please, use CAIT (All Sectors) dataset._

_ **emissions** _ _(\&lt;chr\&gt;): yearly emissions, by sector. In millions of tons of CO __2__ e._

_ **unit** _ _(\&lt;chr\&gt;): unit of emissions data. In this dataset, all numbers are expressed in terms of Mt of CO __2__ e._

1. Global Carbon Project (GCP)

Global Carbon Project (GCP) estimates only carbon dioxide emission for each country. It displays yearly emissions in coal, oil, gas, flaring, cement and other industries, in the 1750 – 2020 period. Although it does not have data for every country since then, [Andrew and Peters (2021)](https://zenodo.org/record/5569235#.YpzABS-B1pS) provides good estimates for high income countries, at least, since the early XIX century.
 GCP data only included CO2e for some industries. LULUCF emissions are estimated only in global level scale. For more comments and methodological comments, check out this [Our World in Data](https://ourworldindata.org/co2-dataset-sources) technical brief. The full GCP methodology is available in [Friedlingstein et al. (2022)](https://www.globalcarbonproject.org/carbonbudget/21/data.htm).

GCP data may be useful to work with long term emissions, given that carbon-dioxide form fuel burning comprehends most of industrial economies past emissions. However, it may be inadequate to work with countries that are high non-CO2 emitters (like Brazil, with its significant cattle ranching methane emissions) and economies with high LULUCF emissions (like Indonesia or Brazil, with significant emissions linked to deforestation).

**GCP (All countries)**: each country yearly CO2 emission, at least, since 1750. Notice that, for most countries, there are no estimates for century back emissions – the first available data are UK&#39;s emissions for 1750.

Source: GCP, with data retrieved from [OWID](https://github.com/owid/co2-data) harmonization.

Coverage: 244 countries, regions and continents, over the 1750 – 2020 period. There is no sectoral specification. It includes global emissions and international transport.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code. Places with no ISO-3c (e.g. Asia (excl. China &amp; India)) are displayed as NA. &quot;INTL&quot; stands for &quot;International Transportation&quot;._

_ **country\_name** _ _(\&lt;chr\&gt;): each country name, in English. Regions and specifications with no ISO-3c (e.g. Asia (excl. China &amp; India)) are displayed here._

_ **emissions** _ _(\&lt;chr\&gt;): yearly emissions, millions of tons of CO __2__._

**GCP (World):** global CO2 emissions since 1750.

Source: GCP, with data retrieved from [OWID](https://github.com/owid/co2-data) harmonization.

Coverage: world (&quot;WLD&quot;), over the 1750 – 2020 period. There is no sectoral specification.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): &quot;WLD&quot; for every row._

_ **country\_name** _ _(\&lt;chr\&gt;): &quot;World&quot; for every row._

_emissions (\&lt;chr\&gt;): yearly emissions, millions of tons of CO __2__._

**GCP:** each country yearly CO2 emission, at least, since 1750.

Source: GCP, with data retrieved from [OWID](https://github.com/owid/co2-data) harmonization.

Coverage: 193 countries, regions and continents, over the 1750 – 2020 period. There is no sectoral specification. It includes international transport, EU27 overall emissions and Kosovo data. Does not include global emissions and EU27 countries standalone emissions.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code. &quot;EUR&quot; stands for EU27. &quot;INTL&quot; stands for International Transportation._

_ **emissions** _ _(\&lt;chr\&gt;): yearly emissions, millions of tons of CO __2__._

_ **unit** _ _(\&lt;chr\&gt;): unit of emissions data. In this dataset, all numbers are expressed in terms of Mt of CO __2__._

1. Emissions Database for Global Atmospheric Research (EDGAR)

EDGAR is the GHG emissions estimates inventory set by the EU Joint Research Center (JRC). On its 6th edition, it covers CO2, CH4 and N2O emissions on the 1970 – 2019 timespan. Data soruces are IEA, FAO, UNFCCC, USGS, NOAA and other institutions. It excluded LULUCF emissions for country level data. For full methodology, check out [this](https://edgar.jrc.ec.europa.eu/dataset_ghg60) document. More detailed data are available on EDGAR&#39;s webpage.

**EDGAR:** countries CO2e emissions, in the 1970 – 2019 period. Only includes CO2, CH4 and N2O emissions. Does not include LULUCF.

Source: [JRC](https://edgar.jrc.ec.europa.eu/). Further reading on methodology available [here](https://edgar.jrc.ec.europa.eu/methodology).

Coverage: 183 countries. It displays EU27, Andorra, Monaco, San Marino and the Vatican emissions under &quot;EUR&quot; ISO3c. Switzerland and Liechtenstein are combined in &quot;CHE, LIE&quot;. Serbia and Montenegro are under &quot;SRB, MNE&quot;. Israel and Palestine, under &quot;ISR, PSE&quot;. International aviation, under &quot;IATA&quot;. International Maritime Transport, under &quot;IMO&quot;. Emissions are detailed in 5 sectors.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code. It does not include World (&quot;WLD&quot;) emissions._

_ **sector** _ _(\&lt;chr\&gt;): sectoral emissions data, organized in 5 categories: &quot;Buildings&quot;, &quot;Transport&quot;, &quot;Power Industry&quot;, &quot;Other industrial combustion&quot; and &quot;Other sectors&quot;._

_ **emissions** _ _(\&lt;chr\&gt;): yearly emissions, by sector. In millions of tons of CO __2__ e._

_ **unit** _ _(\&lt;chr\&gt;): unit of emissions data. In this dataset, all numbers are expressed in terms of Mt of CO __2__ e (100-year GWP of AR4)._

1. 4th _Brazilian National Communication to the UNFCCC_

Each country has autonomy to measure its own emissions, following UNFCCC&#39;s methodological guidelines. These numbers are used by each member to set and follow its climate goal (or Nationally Determined Contribution – NDC). Currently, Brazilian Ministry of Science and Technology has detailed the country&#39;s emission between 1990 and 2016, on a document called &quot;[Quarta Comunicação Nacional do Brasil à UNFCCC](https://issuu.com/mctic/docs/quarta_comunicacao_nacional_brasil_unfccc)&quot;. It covers and details emissions in 5 sectors: Energy, Industrial Processes, Agriculture and Cattle, LULUCF and Waste.
 This is the official Brazilian emissions profile, with very high detailing. It may be useful to use when dealing with the country&#39;s NDC, although its lack of update might be a weakness.

**4CN (All Sectors)
# 2**: SIRENE estimates for Brazilian GHG emissions. It covers CO2, CH4, N2O, CF4, C2F6, HFC-23, HFC125, HFC134a, HFC143a, HFC152a, SF6, CO, NOx e NMVOC, using IPCC&#39;s guidelines. It includes (and details) LULUCF emissions. It used AR5 conversion factors, given that this is the methodology indicated by the Brazilian government on its [NDC](https://unfccc.int/sites/default/files/NDC/2022-06/Updated%20-%20First%20NDC%20-%20%20FINAL%20-%20PDF.pdf).

Source: [SIRENE](https://www.gov.br/mcti/pt-br/acompanhe-o-mcti/cgcl/clima/paginas/sistema-de-registro-nacional-de-emissoes-sirene)

Coverage: Overall Brazilian emissions over the 1990 – 2016 timespan, for 5 sectors and multiple subsectors.

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **sector** _ _(\&lt;chr\&gt;): emission sector and subsector. Notice that there are overlapping data between them._

_ **emissions** _ _(\&lt;chr\&gt;): yearly emissions, by sector and subsector._

_ **unit** _ _(\&lt;chr\&gt;): unit of emissions data. In this dataset, all numbers are expressed in terms of Mt of CO __2__ e (100-year GWP AR5)._

**4CN (Main Sectors)**: SIRENE estimates for Brazilian GHG emissions, for the 5 main sectors: Energy, Agriculture, LULUCF, Industrial Processes and Waste. This is a subset of the previous data frame.

Source: [SIRENE](https://www.gov.br/mcti/pt-br/acompanhe-o-mcti/cgcl/clima/paginas/sistema-de-registro-nacional-de-emissoes-sirene)

Coverage: Overall Brazilian emissions over the 1990 – 2016 timespan, for 5 sectors.

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **sector** _ _(\&lt;chr\&gt;): emission sector and subsector. There is no overlapping data._

_ **emissions** _ _(\&lt;chr\&gt;): yearly emissions, by sector._

_ **unit** _ _(\&lt;chr\&gt;): unit of emissions data. In this dataset, all numbers are expressed in terms of Mt of CO __2__ e (100-year GWP AR5)._

1. Carbon Markets

The establishment of carbon markets guided the phenomenon of carbon pricing. In Emissions Trade Schemes and voluntary markets, there are a growing number of initiatives on it.

**Berkeley Carbon Trading Project:** offsets registrations and retirement, specified by year, project, country and methodology. Berkeley Carbon Trading Project team harmonized and summarized publicly available data from Verra (VCS), Gold Standard (GS), American Carbon Registry (ACR) and Climate Action Reserve (CAR) registered offsets. Notice that the voluntary carbon market has a plenty of other standards, but those are the top compliance ones, in [ICROA&#39;s](https://www.google.com/search?client=safari&amp;rls=en&amp;q=icroa+top+compliance+programs&amp;ie=UTF-8&amp;oe=UTF-8) definition. High level ESG policies, for example, do not accept offsets generated under other standards, due to the high risk of greenwashing.

For a glossary on the VCM terms, check out [this](https://verra.org/wp-content/uploads/2022/01/Program-Definitions_v4.1.pdf) one written by Verra.

Source: [BCTP](https://gspp.berkeley.edu/faculty-and-impact/centers/cepp/projects/berkeley-carbon-trading-project/offsets-database) (v4)

Coverage: credits registered and retired between 1996-01-01 to 2021-12-31

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **id** _ _(\&lt;chr\&gt;): project id, on the XXX#### format, where XXX is the registry (VCS, GS, ACR or CAR) and #### is the project number._

_ **iso3c** _ _(\&lt;chr\&gt;): country ISO-3c code where the project is set_

_ **scope** _ _(\&lt;chr\&gt;): project scope, according to BCTP guidelines. It may be fit into 9 distinct categories._

_ **type** _ _(\&lt;chr\&gt;): project type, according to BCTP guidelines_

_ **credits\_issued** _ _(\&lt;dbl\&gt;): number of credits issued in each year, by each project. Notice that issuance year and registration year may differ. This column refers to year when each credit was added to the common registry._

_ **credits\_retired** _ _(\&lt;dbl\&gt;): number of retirements in each year, for credits issued in each project._

_ **status** _ _(\&lt;chr\&gt;): project current status_

_ **registry** _ _(\&lt;chr\&gt;): registry used to generate project&#39;s offsets. It may be VCS, GS, ACR or CAR._

_ **methodology** _ _(\&lt;chr\&gt;): methodology used by each project. Available only for VCS projects. A full list of VCS approved methodologies is available_ [_here_](https://www.google.com/search?client=safari&amp;rls=en&amp;q=verrra+methodologies&amp;ie=UTF-8&amp;oe=UTF-8)_._

_ **certification** _ _(\&lt;chr\&gt;): additional certification, like CCB and SDVista_

**EU ETS Futures:** EU27 average allowance future price. This is a mean value for this market, since prices are set via auctions and private agents have the right to sell each other carbon emission licenses.

Source: [Trading View](https://www.tradingview.com/symbols/ICEEUR-ECF1%21/)

Coverage: EU ETS, on the Feb/2012 – Feb/2022 period (monthly).
# 3

_ **time** _ _(\&lt;date\&gt;): reference day, in YYYY-MM-DD format. Data available for each month first working day._

_ **close** _ _(\&lt;dbl\&gt;):_ _ECF1!_ _Closing price, in Euros._

**CBL Futures:** agents on the voluntary carbon markets (VCMs) are free to create its own projects and sell offsets to whoever is desired, in private established contracts. However, there are growing efforts to give more centrality to this market. Xpansiv Inc. created and asset composed by VCM offsets that follow some quality guidelines. They called it a CBL Global Emissions Offset (GEO). A GEO is a contract the deliveries an offset generated by a project registered on Verra, ACR or CAR, with CORSIA eligibility. Further details available [here](https://www.cmegroup.com/trading/energy/cbl-global-emissions-offset-futures.html).

CBL Nature-Based Global Emissions Offsets (N-GEOs) are assets structured on the same way, but with stricter compliance restrictions. A NGEO is a Verra registered offset, in AFOLU sector, with Climate, Community and Biodiversity (CCB) label. Also, they must have been generated in recent year vintages. Giver its higher quality, NGEOs prices have a premium gap. Further details [here](https://www.cmegroup.com/education/articles-and-reports/geo-futures-a-natural-solution.html).

Source: Trading View ([GEO](https://www.tradingview.com/symbols/NYMEX-GEO1!/) and [NGO](https://www.tradingview.com/symbols/NYMEX-NGO1%21/))

Coverage: 2021-02-28 to 2022-03-02 (daily).

_ **date** _ _(\&lt;date\&gt;): reference day, in YYYY-MM-DD format. Data available for each working day._

_ **geo1** _ _(\&lt;dbl\&gt;): GEO1__!_ _Closing price, in USD. Current month contract._

_ **geo2** _ _(\&lt;dbl\&gt;): GEO2__!_ _Closing price, in USD. Next month contract._

_ **ngo1** _ _(\&lt;dbl\&gt;): NGO1__!_ _Closing price, in USD. Current month contract._

_ **ngo2** _ _(\&lt;dbl\&gt;): NGO2__!_ _Closing price, in USD. Next month contract._

1.
# Countries Indicators

1. Demographics and Economy

**UN Population (All Locations):** UN populations past and future population estimates. Median values for future population estimates were retrieved. Notice that this dataset only contains numbers for total population, but the UN Department of Economic and Social Affairs has datasets with more detailing. Also, UN&#39;s team has harmonized numbers for countries and regions with borders change over time (e.g: there is no West and East Germany entries, although they were two different entities until 1990. German estimates are united under &quot;DEU&quot; ISO-3c).

Source: [UN Department of Economic and Social Affairs](https://population.un.org/wpp/Download/Standard/CSV/)

Coverage: 474 distinct locations. It accounts data for multiples countries, regional groups and continents. Notice that there are overlapping data. It covers the 1960 – 2100 timespan.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code. Location with no ISO-3C (e.g: BRICS) are filled with NA._

_ **location** _ _(\&lt;chr\&gt;): location name, in English._

_ **population** _ _(\&lt;dbl\&gt;): each location total population median population estimate, in millions of people._

**UN Population (Countries):** UN populations past and future population estimates. Subset of the previous dataset only with country-level data + the EU27. EU countries specific data is not detailed.

Source: [UN Department of Economic and Social Affairs](https://population.un.org/wpp/Download/Standard/CSV/)

Coverage: 207 countries + EU27, on the 1960 – 2100 period.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code. EU27 = &quot;EUR&quot;_

_ **population** _ _(\&lt;dbl\&gt;): each location population median population estimate, in millions of people._

**OECD Long-Term GDP Forecasts:** OECD past GDP figures and future forecasts. GDP displayed in constant 2010 PPP USD, for the world&#39;s main economies. PPP adjustments allow over-time and cross-country comparisons, although we should do it carefully. These data are estimates set with available data today, but it may (and probably will) change in the future, especially in the long-term.
 More details on the methodology [here](https://data.oecd.org/gdp/real-gdp-long-term-forecast.htm#indicator-chart). For more details on different GDP measures, check out this report on [PPP](https://www.imf.org/external/pubs/ft/fandd/basics/ppp.htm), and this one [current vs constant](https://www.investopedia.com/terms/r/realgdp.asp) GDP. Data retrieved in late-2021.

Source: [OECD](https://data.oecd.org/gdp/real-gdp-long-term-forecast.htm#indicator-chart)

Coverage: 54 locations, including some countries groups, like OECD and G20, and global forecast. EU27 data is summarized on &quot;EUR&quot; fictional ISO-3C. EU27 estimates do not include Croatia, Malta and Cyprus data, which corresponds to nearly 0.6% of the total EU27 GDP. Data for the 1990 – 2060 timespan.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code. For special regions, a proxy notation was used._

_ **gdp** _ _(\&lt;dbl\&gt;): GDP, in billions of 2010 PPP USD. Notice that this projection will be updated on every OECD Economic Outlook Report. For same countries in some years, data may be unavailable._

**World Bank GDP:** yearly GDP estimates produced by the World Bank. All data are displayed in constant 2015 USD. Data retrieved in late-2021.

Source: [World Bank](https://data.worldbank.org/indicator/NY.GDP.MKTP.KD)

Coverage: 266 locations, including some countries groups, like OECD and G20. EU27 data is no summarized on this dataset. Data covers the 1960 – 2020 timespan. For some locations in some years, data may be unavailable.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code. Locations with no ISO-3C (e.g: Asia) are filled with NA._

_ **location** _ _(\&lt;chr\&gt;): location name, in English._

_ **gdp** _ _(\&lt;dbl\&gt;): \&gt;): GDP, in billions of 2015 USD (not PPP-adjusted)._

**World Bank GDP (Countries):** yearly GDP estimates produced by the World Bank, retrieved from the previous dataset. It excludes non-countries and includes EU27 data.

Source: [World Bank](https://data.worldbank.org/indicator/NY.GDP.MKTP.KD)

Coverage: 184 countries + EU27. It included EU27 countries individual data. Data covers the 1960 – 2020 timespan. For some locations in some years, data may be unavailable.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code. EU27 = &quot;EUR&quot;_

_ **gdp** _ _(\&lt;dbl\&gt;): \&gt;): GDP, in billions of 2015 USD (not PPP-adjusted)._

**Urban Population Ratio:** proportion of population living in cities, as a ratio (0 – 100%) of total population.

Source: [World Bank](https://data.worldbank.org/indicator/SP.URB.TOTL.IN.ZS)

Coverage: 202 countries, over the 1961 – 2020 timespan. Does not include EU27 aggregate data.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code. EU27 = &quot;EUR&quot;_

_ **income\_group** _ _(\&lt;chr\&gt;): each country World Bank income group._

_ **urban\_ratio** _ _(\&lt;dbl\&gt;): urban population, as a fraction of total country population. It varies between 0 and 100._

1. Environment and Agriculture

**Countries Food Production:** FAO&#39;s estimates for yearly production, for each country, for each crop and food type. Data retrieved in early-2022.

Source: [Food and Agriculture Organization (FAO)](https://www.fao.org/faostat/en/#data)

Coverage: 216 countries and regions, over the 1960 – 2021 timespan. Does not include EU27 aggregate data. Mora details on FAO&#39;s definitions [here](https://www.fao.org/faostat/en/#definitions).

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code._

_ **code\_item** _ _(\&lt;dbl\&gt;): item reference code. There are 300 available on FAO&#39;s database._

_ **name\_item** _ _(\&lt;chr\&gt;): item name._

_ **element** _ _(\&lt;chr\&gt;): analyzed item element. It may be &quot;Area Harvested&quot;, &quot;Yield&quot;, &quot;Production&quot;, &quot;Stocks&quot;, &quot;Yield/Carcass Weight&quot;, &quot;Producing Animals/Slaughtered&quot;, &quot;Milk Animals&quot;, &quot;Laying&quot; or &quot;Prod Popultn&quot;._

_ **value** _ _(\&lt;dbl\&gt;): value of the reference element item._

_ **unit** _ _(\&lt;chr\&gt;): unit of the referent element item. It may be &quot;ha&quot;, &quot;hg/ha&quot;, &quot;tonnes&quot;, &quot;Head&quot;, &quot;hg/An&quot;, &quot;1000 Head&quot;, &quot;0.1g/An&quot;, &quot;100mg/An&quot;, &quot;No/An&quot;, &quot;1000 No&quot;, &quot;No&quot; or &quot;hg&quot;._

_ **flag** _ _(\&lt;chr\&gt;): detailing on data source. Further reading_ [_here_](https://www.fao.org/faostat/en/#definitions)_._

**Countries Land Use:** FAO&#39;s estimates for yearly land use, by country. It displays estimates for area dedicated to activies like cropping, cattle raising and forest preservation. Full list available [here](https://www.fao.org/faostat/en/#definitions) (or in the dataset). Data retrieved in early-2022.

Source: [Food and Agriculture Organization (FAO)](https://www.fao.org/faostat/en/#data)

Coverage: 230 countries and regions, over the 1960 – 2019 timespan. It includes EU27 aggregate data. Mora details on FAO&#39;s definitions [here](https://www.fao.org/faostat/en/#definitions).

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code._

_ **code\_item** _ _(\&lt;dbl\&gt;): item reference code. There are 45 available on FAO&#39;s database._

_ **name\_item** _ _(\&lt;chr\&gt;): item name._

_ **area** _ _(\&lt;dbl\&gt;): reference item area, in thousand hectares (for item &quot;Forest land&quot; – code 6646 – the element measured is &quot;Carbon stock in living biomass&quot;, displayed in million tons of carbon)_

**Countries Land Cover:** FAO&#39;s estimates for yearly land cover, by country. It displays estimates for surface coverage. Data retrieved in early-2022.

Source: [Food and Agriculture Organization (FAO)](https://www.fao.org/faostat/en/#data)

Coverage: 233 countries and regions, over the 1960 – 2019 timespan. It does not include EU27 aggregate data. Mora details on FAO&#39;s definitions [here](https://www.fao.org/faostat/en/#definitions).

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format._

_ **iso3c** _ _(\&lt;chr\&gt;): each country ISO-3C code._

_ **code\_item** _ _(\&lt;dbl\&gt;): item reference code. There are 45 available on FAO&#39;s database._

_ **name\_item** _ _(\&lt;chr\&gt;): item name._

_ **name\_element** _ _(\&lt;chr\&gt;): reference item source._

_ **area** _ _(\&lt;dbl\&gt;): reference item area, in thousand hectares._

1.
# Brazil in Numbers

1. Demographics and Economy

**Municipalities Population:** Estimates for each city population by July 1st. It gathers data from decennial census, 2007 Population Count and Yearly Population Estimates. There are no population estimates for cities before its emancipation (e.g: there are no prior-2012 records for Mojuí dos Campos (PA), which elected its first mayor in 2012). For further information on IBGE&#39;s city level data, check out [IBGE Cidades.](https://cidades.ibge.gov.br/)

Source: IBGE ([Census](https://sidra.ibge.gov.br/pesquisa/censo-demografico/demografico-2010/inicial) in 2010, [Population Count](https://www.ibge.gov.br/estatisticas/sociais/habitacao/9065-contagem-da-populacao.html?=&amp;t=resultados) in 2007 and [Population Estimates](https://sidra.ibge.gov.br/pesquisa/estimapop/tabelas) for the other years)

Coverage: 5570 municipalities, for the 2001 – 2021 period.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code_

_ **id\_immediate\_region** _ _(\&lt;dbl\&gt;): 6-number immediate region code_

_ **id\_municipality** _ _(\&lt;dbl\&gt;): 7-number city code_
_ **population** _ _(\&lt;dbl\&gt;): total resident population, in absolute terms, by July 1__st_ _or census/population count survey date. It accounts for the total number of inhabitants in each municipality each year._

**Municipalities Sectoral GDP:** estimates for each city sectoral GDP. On the Brazilian System of National Accounts, aggregate expenditure is composed by 4 sectors: industry, agriculture and cattle raising, services (excl. public administration) and public administration. For further reading, check out IBGE&#39;s methodology. GDP is the sum of these four sectors with taxes. Further readings on methodology available [here](https://www.ibge.gov.br/estatisticas/economicas/contas-nacionais/9088-produto-interno-bruto-dos-municipios.html?=&amp;t=notas-tecnicas).

Source: [IBGE](https://www.ibge.gov.br/estatisticas/economicas/contas-nacionais/9088-produto-interno-bruto-dos-municipios.html?=&amp;t=o-que-e)

Coverage: 5570 municipalities, for the 2002 – 2019 period.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_municipality** _ _(\&lt;dbl\&gt;): 7-number city code_

_ **id\_immediate\_region** _ _(\&lt;dbl\&gt;): 6-number immediate region in which the city is located_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code in which the city is located_
_ **population** _ _(\&lt;dbl\&gt;): total resident population, in absolute terms, by July 1__st_ _or census/population count survey date._

_ **sector** _ _(\&lt;chr\&gt;): reference sector data. Notice that there are overlapping data._

_ **gdp** _ _(\&lt;dbl\&gt;): current GDP, in thousand BRL (not inflation-adjusted)._

_ **gdp\_deflator** _ _(\&lt;dbl\&gt;): constant GDP, in 2021 thousand BRL (inflation-adjusted with GDP implicit deflator)._

_ **gdp\_ipca** _ _(\&lt;dbl\&gt;): constant GDP, in 2020 thousand BRL (inflation-adjusted with IPCA – Brazilian main CPI index)_

_ **gdppc\_deflator** _ _(\&lt;dbl\&gt;): constant per capita GDP, in 2021 thousand BRL (inflation-adjusted with GDP implicit deflator)._

_ **gdp\_ipca** _ _(\&lt;dbl\&gt;): constant GDP per capita, in 2020 thousand BRL (inflation-adjusted with IPCA – Brazilian main CPI index)_

**Municipalities GDP:** subset of the previous series only with global GDP, for each municipality. Cities that were established after 2002 does not show data for pre-creation period.

Source: [IBGE](https://www.ibge.gov.br/estatisticas/economicas/contas-nacionais/9088-produto-interno-bruto-dos-municipios.html?=&amp;t=o-que-e)

Coverage: 5570 municipalities, for the 2002 – 2019 period.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_municipality** _ _(\&lt;dbl\&gt;): 7-number city code_

_ **id\_immediate\_region** _ _(\&lt;dbl\&gt;): 6-number immediate region in which the city is located_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code in which the city is located_
_ **population** _ _(\&lt;dbl\&gt;): total resident population, in absolute terms, by July 1__st_ _or census/population count survey date._

_ **gdp** _ _(\&lt;dbl\&gt;): current GDP, in thousand BRL (not inflation-adjusted)._

_ **gdp\_deflator** _ _(\&lt;dbl\&gt;): constant GDP, in 2021 thousand BRL (inflation-adjusted with GDP implicit deflator)._

_ **gdp\_ipca** _ _(\&lt;dbl\&gt;): constant GDP, in 2020 thousand BRL (inflation-adjusted with IPCA – Brazilian main CPI index)_

_ **gdppc\_deflator** _ _(\&lt;dbl\&gt;): constant per capita GDP, in 2021 thousand BRL (inflation-adjusted with GDP implicit deflator)._

_ **gdp\_ipca** _ _(\&lt;dbl\&gt;): constant GDP per capita, in 2020 thousand BRL (inflation-adjusted with IPCA – Brazilian main CPI index)_

**Bolsa Família:** Bolsa Familia Programs (BFP) is a large-scale cash transfers program set by the Brazilian Federal Government. It gives monthly paychecks for families with monthly per capita income below BRL 89, or BRL 178 (if the household has children or teenagers). It is good real-time proxy for extreme poverty, since only people on misery status are allowed to receive it. Original data is supplied on a month-level period, with families subscribed and cash transfers for each city. Notice that the amount of cash transfers is based on factors like household size and household composition. For more details on BFP rules, check out [this](https://www.gov.br/cidadania/pt-br/acoes-e-programas/outros/bolsa-familia) website. Although the series continues after 2019, due to the Covid-19 pandemic (and Brazilian paycheck policy) and changes on the programs structure, we decided to end this timeseries before in December 2019.

Source: [Ministério da Cidadania](https://dados.gov.br/dataset/bolsa-familia-misocial), via Portal Brasileiro de Dados Abertos

Coverage: 5570 municipalities, for the 2004 – 2019 period. Original dataset displays monthly cash transfers.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_municipality** _ _(\&lt;dbl\&gt;): 7-number city code_

_ **id\_immediate\_region** _ _(\&lt;dbl\&gt;): 6-number immediate region in which the city is located_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code in which the city is located_
_ **population** _ _(\&lt;dbl\&gt;): total resident population, in absolute terms, by July 1__st_ _or census/population count survey date._

_ **average\_families** _ _(\&lt;chr\&gt;): average number of families subscribed in each year. The amount of household receving cash transfers may change year-round, as well as the number of residents in each household. This column displays an arithmetic mean of families enrolled on BFP in each year, for each city._

_ **cash\_transfers** _ _(\&lt;dbl\&gt;): total amount of BFP cash transfers in each year, for each city (in nominal BRL)._

_ **cash\_transfers\_pc** _ _(\&lt;dbl\&gt;): ratio between yearly cash transfers and municipality population. Notice that not every city dweller receives BPF transfers. This is a proxy to compare poverty in each city constantly, as Brazilian census are done in every ten years and PNAD does not detail city level development status. Cities with high cash transfers per capita are more likely to be, on average, poorer._

_ **ipca\_cash\_transfers** _ _(\&lt;dbl\&gt;): BFP total cash tranfers, for each city in each year, in December 2020 BRL (inflation adjusted with IPCA)_

_ **ipca\_cash\_transfers\_pc** _ _(\&lt;dbl\&gt;): cash transfers per capita, in December 2020 BRL (inflation adjusted with IPCA)_

**PNAD Total Income:** PNAD (Pesquisa Nacional por Amostra de Domicílio) is Brazilian main household survey. It shows, quarterly, the living standards of Brazilin population, by income group and location. Every year, it also displays income levels by income deciles. This survey is a good proxy for income level and income distribution on state level data. It only accounts for inhabitants over 14 years old.
 For further methodology issues, check out [IBGE&#39;s](https://www.ibge.gov.br/estatisticas/sociais/habitacao/17270-pnad-continua.html?=&amp;t=conceitos-e-metodos) FAQ. [Hoffmann (2019)](https://iepecdg.com.br/wp-content/uploads/2019/02/RDABR17C.pdf) also discuss and highlights important aspects of Brazilian income distribution.

Source: [IBGE](https://sidra.ibge.gov.br/tabela/7427) (Tabela 7427)

Coverage: 27 states + Brazil, for the 2012 – 2019 period.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code. Brazil = 1_

_ **income\_group** _ _(\&lt;chr\&gt;): reference income group decile. For extreme groups ( \&lt; 10% and \&gt;90%), there are also quintiles and centiles specification._

_ **total\_income** _ _(\&lt;dbl\&gt;): sum of all income sources of people in this group. Notice that a decile corresponds to 10% of Brazilian inhabitants, or nearly 20 million people for the last ten years. The income of the &quot;Maior que P90&quot; group is the sum of all income sources of the richest 10% Brazilians. Values in millions BRL (not inflation-adjusted)._

_ **ipca\_total\_income** _ _(\&lt;dbl\&gt;): sum of all income sources of people in this group. Values in 2020 millions BRL (IPCA inflation-adjusted)._

**PNAD Population Income:** total of people in every decile (or quintile, or centile) of income. Notice that is a static value. 10% of the Brazilian inhabitants corresponds to nearly 20% people, every year, since 2012. Minor changes may be noticed.

Source: [IBGE](https://sidra.ibge.gov.br/tabela/7521) (Tabela 7521)

Coverage: 27 states + Brazil, for the 2012 – 2019 period.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code. Brazil = 1_

_ **income\_group** _ _(\&lt;chr\&gt;): reference income group decile_

_ **population** _ _(\&lt;dbl\&gt;): sum of working population in every income group._

**PNAD Mean Income:** average income level for every income group. This is the arithmetic mean between the sum of income and the sum of population, for each income group. It does not show intra-group inequality. Notice that the mean value is not the median value. This dataset includes children headcount.

Source: [IBGE](https://sidra.ibge.gov.br/tabela/7531) (Tabela 7531)

Coverage: 27 states + Brazil, for the 2012 – 2019 period.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code. Brazil = 1_

_ **income\_group** _ _(\&lt;chr\&gt;): reference income group decile_

_ **mean\_income** _ _(\&lt;dbl\&gt;): mean income level in each group (not inflation-adjusted)._

_ **ipca\_mean\_income** _ _(\&lt;dbl\&gt;): mean income level in each group. Values in 2020 constant BRL (IPCA inflation-adjusted)._

**PNAD Upper bound Income:** monthly income needed to be the richest person in each group. (E.g: if the P10 upper bound is 200 BRL, someone with a BRL 201 BRL income is part of the P10 to P20 decile)

Source: [IBGE](https://sidra.ibge.gov.br/tabela/7438) (Tabela 7538)

Coverage: 27 states + Brazil, for the 2012 – 2019 period.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code. Brazil = 1_

_ **income\_group** _ _(\&lt;chr\&gt;): reference income group decile_

_ **upperbound\_income** _ _(\&lt;dbl\&gt;): income needed to be the upper bound group cutoff, in nominal BRL (not inflation-adjusted)._

_ **ipca\_mean\_income** _ _(\&lt;dbl\&gt;): income needed to be the upper bound group cutoff, in 2020 BRL (IPCA inflation-adjusted)._

**Unemployment by age:** quarterly unemployment rate (and population aggregates), by age group. It Only accounts for over 14-year-old citizens. Notice that IBGE&#39;s uses a [specific](https://www.ibge.gov.br/explica/desemprego.php) definition of unemployment.

Source: [IBGE](https://sidra.ibge.gov.br/tabela/4094) (Tabela 4094)

Coverage: 27 states + Brazil, for the Q12012 – Q32021 period.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **quarter** _ _(\&lt;dbl\&gt;): referece quarter. 1 = first (Jan to Mar), and 4 = fourth (Oct to Dec)_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code. Brazil = 1_

_ **age\_group** _ _(\&lt;chr\&gt;): reference age group._

_ **total\_people** _ _(\&lt;dbl\&gt;): estimate of people in reference age group. In millions._

_ **occupied** _ _(\&lt;dbl\&gt;): estimate for occupied people in reference group age. In millions._

_ **non\_occupied** _ _(\&lt;dbl\&gt;): estimate for people not-working in reference age group. In millions. Notice that this is not the total number &quot;unemployed&quot; people._

_ **no\_working** _ _(\&lt;dbl\&gt;): estimate for people that is not work, but it is in the working age, by age group. In millions._

_ **unemployment\_rate** _ _(\&lt;dbl\&gt;): (non\_occupied/(non\_occupied+occupied)) x 100. It does not count people who can work but does not seek a job position. It varies between 0 and 100._

**Unemployment:** subset of the previous data frame, filtering only for states totals

Source: [IBGE](https://sidra.ibge.gov.br/tabela/4094) (Tabela 4094)

Coverage: 27 states + Brazil, for the Q12012 – Q32021 period.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **quarter** _ _(\&lt;dbl\&gt;): referece quarter. 1 = first (Jan to Mar), and 4 = fourth (Oct to Dec)_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code. Brazil = 1_

_ **total\_people** _ _(\&lt;dbl\&gt;): estimate of people in reference. In millions._

_ **occupied** _ _(\&lt;dbl\&gt;): estimate for occupied people in reference. In millions._

_ **non\_occupied** _ _(\&lt;dbl\&gt;): estimate for people not-working in reference age group. In millions. Notice that this is not the total number &quot;unemployed&quot; people._

_ **no\_working** _ _(\&lt;dbl\&gt;): estimate for people that is not work, but it is in the working age. In millions._

_ **unemployment\_rate** _ _(\&lt;dbl\&gt;): (non\_occupied/(non\_occupied+occupied)) x 100. It does not count people who can work but does not seek a job position. It varies between 0 and 100._

**Education Level:** totals of people, by forma education level. Only accounts for people over 14-years-old.

Source: [IBGE](https://sidra.ibge.gov.br/tabela/7128) (Tabela 7128)

Coverage: 27 states + Brazil, for the 2016 – 2019 period.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code. Brazil = 1_

_ **education\_level** _ _(\&lt;dbl\&gt;): estimate of people in education level group. It goes from &quot;no education&quot; to &quot;college graduated&quot;. In thousands._

_ **population\_pct** _ _(\&lt;dbl\&gt;): ratio of each group education level, as part of total state population._

1. Environment and Agriculture

**Amazon Deforestation:** INPE (Instituto Nacional de Pesquisas Espaciais) estimates for deforestation in the Amazon Biome. PRODES estimates aggregate deforestation increase between august of year T-1 and July of T. That is: the 5257 sq. km of deforestation increase in Pará in 2021 corresponds to data collected between 2020-08-01 and 2021-07-31. Pre-1995 may be inconsistent. Further details [here](http://www.obt.inpe.br/OBT/assuntos/programas/amazonia/prodes/pdfs/Metodologia_Prodes_Deter_revisada.pdf).

Source: [PRODES](http://terrabrasilis.dpi.inpe.br/app/dashboard/deforestation/biomes/legal_amazon/increments). Data retrieved from Terrabrasilis Portal

Coverage: 9 Legal Amazon states (AM, AP, PA, AP, RR, RO, TO, MA and MT), over the 1988 – 2021 period.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code._

_ **deforestation\_increase** _ _(\&lt;dbl\&gt;): increase in deforested area, due to human activity (&quot;corte raso&quot;, in Portuguese). In sq. km._

**Amazon Deforestation (Yearly):** subset with previous dataset, summing up every state data. Notice that Amazon Biome and Legal Amazon does not account for the same region. PRODES data does not measure deforestation in the Cerrado biome of Tocantins (which is part of the Legal Amazon, but not the Amazon Biome).

Source: [PRODES](http://terrabrasilis.dpi.inpe.br/app/dashboard/deforestation/biomes/legal_amazon/increments). Data retrieved from Terrabrasilis Portal

Coverage: Amazon Biome, over the 1988 – 2021 period.

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **deforestation\_increase** _ _(\&lt;dbl\&gt;): increase in deforested area, due to human activity (&quot;corte raso&quot;, in Portuguese). In sq. km._

**Deforestation Cities Blacklist:** cities in added on &quot;Lista de Municípios Prioritários&quot;, coined by the Ministry of Environment. These are cities in the Amazon with large deforestation increases, both in absolute and change terms. Further reading on its nature and its effects on deforestation are found in [Assunção and Rocha (2019)](https://www.cambridge.org/core/journals/environment-and-development-economics/article/abs/getting-greener-by-going-black-the-effect-of-blacklisting-municipalities-on-amazon-deforestation/360C7CAB41129B18FEE2D37C66317914).

Source: Brazilian [Ministry of Environment](https://www.gov.br/mma/pt-br/assuntos/servicosambientais/controle-de-desmatamento-e-incendios-florestais/municipios-prioritarios) (MMA)

Coverage: Amazon Biome, since 2008 (last update in late-2021).

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_municipality** _ _(\&lt;dbl\&gt;): 7-number city code_

_ **name\_municipality** _ _(\&lt;chr\&gt;): reference city name_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code_

_ **year\_enter** _ _(\&lt;dbl\&gt;): year of first inclusion_

_ **year\_withdraw** _ _(\&lt;dbl\&gt;): city removal year from the list_

_ **year\_return** _ _(\&lt;dbl\&gt;): year of return to the list. Cities like Marcelândia (MT) and Querência (MT) were sucessfu on tackling deforestation, but recent spikes made them a return to the list. For those cities, year\_withdraw = NA._

**Mapbiomas:** highly detailed data on Brazilian cities land cover. Mapbiomas team uses high quality images (30-meter resolution) to gather information on land cover, for every Brazilian city, in every biome. Older data may not be as clever as the actual.

Source: [Mapbiomas](https://mapbiomas.org/download) (V6)

Coverage: 5570 cities, on the 1985 – 2020 period

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_municipality** _ _(\&lt;dbl\&gt;): 7-number city code_

_ **id\_immediate\_region** _ _(\&lt;dbl\&gt;): 6-number immediate region in which the city is located_

_ **name\_municipality** _ _(\&lt;chr\&gt;): reference city name_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code_

_ **level\_zero** _ _(\&lt;chr\&gt;): first level of land cover aggregation (anthropic, natural or not applied)_

_ **level\_one** _ _(\&lt;chr\&gt;): second level of land cover aggregation. Six possibilities._

_ **level\_two** _ _(\&lt;chr\&gt;): third level of land cover aggregation. 20 possibilities._

_ **level\_three** _ _(\&lt;chr\&gt;): fourth level of land cover aggregation. 21 possibilities._

_ **level\_four** _ _(\&lt;chr\&gt;): fifth level of land cover aggregation. 26 possibilities._

_ **area** _ _(\&lt;dbl\&gt;): every level correspondent area, for each city, in sq. km._

**Mapbiomas (States):** subset of the previous data frame, with state aggregation.

Source: [Mapbiomas](https://mapbiomas.org/download) (V6)

Coverage: 5570 cities, on the 1985 – 2020 period

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code_

_ **level\_zero** _ _(\&lt;chr\&gt;): first level of land cover aggregation (anthropic, natural or not applied)_

_ **level\_one** _ _(\&lt;chr\&gt;): second level of land cover aggregation. Six possibilities._

_ **level\_two** _ _(\&lt;chr\&gt;): third level of land cover aggregation. 20 possibilities._

_ **level\_three** _ _(\&lt;chr\&gt;): fourth level of land cover aggregation. 21 possibilities._

_ **level\_four** _ _(\&lt;chr\&gt;): fifth level of land cover aggregation. 26 possibilities._

_ **area** _ _(\&lt;dbl\&gt;): every level correspondent area, for each city, in sq. km._

**Mapbiomas (Level Zero):** subset of the complete data frame, only with level zero aggregation (anthropicor natural areas).

Source: [Mapbiomas](https://mapbiomas.org/download) (V6)

Coverage: 5570 cities, on the 1985 – 2020 period

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code_

_ **level\_zero** _ _(\&lt;chr\&gt;): first level of land cover aggregation (anthropic, natural or not applied)_

_ **area** _ _(\&lt;dbl\&gt;): every level correspondent area, for each city, in sq. km._

**Mapbiomas (Level One):** subset of the complete data frame, with level zero (anthropic or natural areas) and level one (forest, natural non-forest, farming, non-vegetated area, water and non-observed).

Source: [Mapbiomas](https://mapbiomas.org/download) (V6)

Coverage: 5570 cities, on the 1985 – 2020 period

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code_

_ **level\_zero** _ _(\&lt;chr\&gt;): first level of land cover aggregation (anthropic, natural or not applied)_

_ **level\_one** _ _(\&lt;chr\&gt;): second level of land cover aggregation. Six possibilities._

_ **area** _ _(\&lt;dbl\&gt;): every level correspondent area, for each city, in sq. km._

**Pesquisa Pecuária Municipal (PAM):** cattle herd estimates, for each municipality by december 31st. Older data may lack consistency.

Source: [IBGE](https://sidra.ibge.gov.br/Tabela/3939) (tabela 3939)

Coverage: 5570 cities, on the 1974 – 2020 period

Columns Description:

_ **year** _ _(\&lt;dbl\&gt;): reference year, in YYYY format_

_ **id\_municipality** _ _(\&lt;dbl\&gt;): 7-number city code_

_ **id\_immediate\_region** _ _(\&lt;dbl\&gt;): 6-number immediate region in which the city is located_

_ **name\_municipality** _ _(\&lt;chr\&gt;): reference city name_

_ **id\_state** _ _(\&lt;dbl\&gt;): 2-number state code_

_ **herd\_type** _ _(\&lt;chr\&gt;): type of reference cattle herd. Eight possible options._

_ **headcount** _ _(\&lt;dbl\&gt;): sum of reference herd type, in each city, by December 31 __st__. Cities with no data are filled with zeros._

[1](#sdfootnote1anc) For further reading, check out [Our World in Data](https://ourworldindata.org/world-region-map-definitions) article on global regionalization.

[2](#sdfootnote2anc) &quot;CN&quot; stands for &quot;Comunicação Nacional&quot;, or UNFCCC member own update of its emissions.

[3](#sdfootnote3anc) It is possible to download more recent and daily data by signing up Trading View Pro.
