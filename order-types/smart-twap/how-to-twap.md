# ⏱️ How to TWAP

{% tabs %}
{% tab title="Order Parameters" %}
<figure><img src="../../.gitbook/assets/1 (1).png" alt="" width="332"><figcaption><p>TWAP Order Parameters</p></figcaption></figure>

<table><thead><tr><th width="65">#</th><th>Parameter Name</th><th>Example</th><th>Explanation</th></tr></thead><tbody><tr><td>1.</td><td>Input and Output Token</td><td>AVAX / USDT</td><td>The tokens that you are looking to trade</td></tr><tr><td>2.</td><td>Duration</td><td>10 Minutes</td><td>The time horizon over which you wish to complete your TWAP order. The longer the duration, the lower the price impact.</td></tr><tr><td>3.</td><td>Price Protection</td><td>1% / 5% / 10%</td><td>If the price drops below/above the limit price, the TWAP will automatically pause transactions until the price returns above/below the limit price. If enabled, the TWAP may not be fully completed within the designated duration.</td></tr><tr><td>4.</td><td>Slippage</td><td>1% / 5% / 10%</td><td>The difference between the expected price and executed price of the transaction.</td></tr><tr><td>5.</td><td>Clip Size Type</td><td>Automatic / Absolute / Percentage / Number of Child Orders</td><td>Clip size refers to the size of the child orders. By default, it is automatic - we calculate the clip size based on historical data of trade volumes and order-book depths to create digestible chunks.</td></tr><tr><td>6.</td><td>Advanced Settings</td><td>Trigger Price</td><td><p>The TWAP will only start when the trigger price is reached. For example,</p><p>the current price of ETH is $2000 and I want to sell it. I set my trigger price for $2500. This means that the TWAP will only start when the price of $ETH reaches $2500. </p></td></tr></tbody></table>
{% endtab %}

{% tab title="Advanced Settings" %}
### Clip Size Type

| Clip Size Type         | Explanation                                                                                                                                                                                                                                                               |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Automatic              | The optimal clip size is calculated automatically based on the historical data of trade volume and order-book depth to create the digestible chunks for each order.                                                                                                       |
| Absolute               | <p>Create digestible chunks by the absolute value of the sell token in the trading pair. <br></p><p>For example, I wish to buy $1000 of ETH with USDT. If I input the absolute clip size value as “100”, I am creating 10 child orders that are worth $100 USDT each.</p> |
| Percentage             | <p>Create digestible child orders by the percentage of order size.<br></p><p>For example, 10% clip size generates 10 child orders. 25% clip size will generate 4 child orders and so on.</p>                                                                              |
| Number of Child Orders | <p>Break the parent order into the number of child orders as you please.<br><br>If you’re buying $1000 of a particular asset, inputting 5 child orders will result in the clip size being $200 each. </p>                                                                 |

### Trigger Price

| Trigger Price           | Explanation                                                                                                |
| ----------------------- | ---------------------------------------------------------------------------------------------------------- |
| Trigger Condition Above | Utilise when the trigger price is above the current market price. Typically, this is used for sell orders. |
| Trigger Condition Below | Utilise when the trigger price is below the current market price. Typically, this is used for buy orders.  |
{% endtab %}
{% endtabs %}
