# 💰 How to DCA

{% tabs %}
{% tab title="Order Parameters" %}
<figure><img src="../../.gitbook/assets/twap.fi dca order panel.png" alt="" width="329"><figcaption><p>DCA Order Parameters</p></figcaption></figure>

<table><thead><tr><th width="65">#</th><th>Parameter Name</th><th>Example</th><th>Explanation</th></tr></thead><tbody><tr><td>1.</td><td>Input and Output Token</td><td>AVAX / USDT</td><td>The tokens that you are looking to trade</td></tr><tr><td>2.</td><td>Frequency</td><td>10 Minutes</td><td>The time gap between each purchase. If you wish to invest $100 daily for the next 10 days, your frequency will be 1 Day. Maximum time gap between each purchase for a DCA order is 1 Month.</td></tr><tr><td>3.</td><td>Duration</td><td>3 Hours</td><td>The time horizon over which your DCA order will be completed</td></tr><tr><td>4.</td><td>Start Day &#x26; Time</td><td>12/07/2023 &#x26; 05:05 UTC</td><td>The date and time at which you wish to start your DCA order. Users will have an option to start the DCA order right away by clicking on “Now”</td></tr></tbody></table>
{% endtab %}

{% tab title="Advanced Settings" %}
### Price protection

If the price drops below/above the limit price, **the TWAP will automatically pause transactions until the price returns above/below the limit price.** If enabled, the TWAP may not be fully completed within the designated duration.

**The limit price for price protection will be calculated as a percentage of the market price.** Let's assume the price of WETH/USDT is currently at $2300.\
\
If you are buying WETH with a price protection of 5%, your limit price will be above the current market price and will be set as $2415 (1.05\*2300). If you are selling WETH with a price protection of 10%, your limit price be below the current market price and will be set as $2070 (0.90\*2300). **The limit price will adapt itself based on the price protection percentage and the order direction.**&#x20;
{% endtab %}
{% endtabs %}
