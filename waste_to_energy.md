<h1>Waste to Energy</h1>

<h2>Background</h2>

<p>
    The Waste to Energy case study is a model involving a system of CAFOs, technology sites, and demand nodes. The CAFOs act as the suppliers of cow manure. They can choose to either process the cow manure at a technolocy site or dispose of it at a disposal facility. 
</p>

<img src="Pictures\waste_to_energy\map.png">

<br>

<p>
    The technology sites contain anaerobic digestion and electricity generation technologies (shown below) which are able to process cow manure into bio-electricity and digestate. The digestate is a waste product that can be applied to cropfields or disposed of, and the bio-electricity can be sold to and used by customers. 
</p>

<img src="Pictures\waste_to_energy\tech.png">

<br>

<p>
    Given this system, we would like to know (1) how much waste is processed by the technology sites, (2) how much bio-electricity is produced, (3) and if this system profitable (i.e. do we earn more money from selling bio-electricity than we pay through transportation and operating costs?)
</p>

<p>
    Running this system through ADAM will give us the optimal (i.e. most economically favorable) result. However, this does not mean that the system will be profitable; sometimes the most favorable result is the one with the least losses. When the transportation and operating costs outweigh the earnings from selling bioelectricity, CAFOs will not process any of their waste and instead will choose to dispose of it. In order to encourage CAFOs to process their waste, the price of bio-electricity must be adjusted so that processing the waste is profitable. 
</p>

<p>
    In this case study, we will analyze the effect of three different electricity prices: low price, market price, and high price.
</p>


<h2>Low Electricity Price</h2>

<p>
    In the low electricity price scenario, all CAFOs decide to dispose of all cow manure rather than processing it into bio-electricity. This is shown on the map through the black lines going from each CAFO to the disposal node. 
</p>

<img src="Pictures\waste_to_energy\low_elec.png">

<p>
    This indicates that the price of bio-electricity is so low that the CAFOs would rather dipose of the waste rather than process it. If you were to double-click on the CAFOs, you would find that the price of the supplying the manure is negative for each CAFO, which indicates that each CAFO is losing money by supplying waste. Additionally, the disposal facility is purchasing the manure at zero cost. This means that the CAFOs will suffer a smaller loss if they simply disposed of the waste than attempted to process it. 
</p>

<h2>Market Electricity Price</h2>

<p>
    The next case we will look at is the market price scenario. Market price indicates that the electricity price is set such that it reflects the actual electricity price.
</p>

<p>
    The results, which are displayed below, shows identical results to the Low Electricity Price scenario. This demonstrates that current electricity prices are still not high enough to incentivize CAFOs to process their waste. 
</p>

<img src="Pictures\waste_to_energy\market_elec.png">

<h2>High Electricity Price</h2>

<p>
    The final case we will look at is the high electricity price scneario. The results, which are displayed in the map below, show that two out of the three CAFOs are now willing to process at least part of their waste. You may hover over the transportation routes to see how much of each product is being transported. 
</p>

<img src="Pictures\waste_to_energy\high_elec.png">

<p>
    CAFO1 continues to send all their waste to the disposal facility and does not process any waste, CAFO2 sends 9,600 tonnes of manure per year to Tech1 for processing, and CAFO3 sends all of the manure (15,000 tonnes) to Tech2 for processing. 
</p>

<p>
    Using the cow manure, Tech1 is able to generate 300,000 kWh of bioelectricity per year, and Tech2 is able to generate 467,600 kWh of bioelectricity per year. The disgestate waste product is sent to a waste disposal facility.
</p>

<p>
    Since we do not know the exact price of the bio-electricity, we cannot determine whether or not the system is profitable. We can only determine that this situation is one where losses are minimized. 
</p>

<h2>Conclusion</h2>

<p>
    Low and current market price is not enough incentive for CAFOs to process their waste into energy. It is only when high prices are applied to bio-electricity that CAFOs will begin to process part of their waste into bio-electricity. 
</p>

