# Apriori-Algorithm
Market Basket Analysis on a super market dataset using Apriori Algorithm.

**Aproiri Algorithm** is an Association analysis basically helps to determine the ‘association’ between different items whether it be Grocery, Medical Science, Super Market, etc. Association rule mining is a technique to identify underlying relations between different items. <br/>
_Example: list of items purchased by customers, details of website which are frequently visited etc._

**Apriori Algorithm has three parts:**
1. **Support –** Support shows how frequent the item ‘I1’ and ‘I2’ occurs with respect to all transaction happen in a given period. <br/>
( Number of transactions containing item I ) / ( Total number of transactions )
2. **Confidence -** Confidence indicate how often the ‘I1’ & ‘I2’ occur together given the number of times ‘I1’ occurs. <br/>
( Number of transactions containing I1 and I2 ) / ( Number of transactions containing I1 )
3. **Lift –** List is the strength of any rule. It gives independence occurance probability of ‘I1’ and ‘I2’. <br/>
( Confidence( I1 -> I2 ) / ( Support(I2) )

**Apriori Principle** <br/>
Here, an item-set is called frequent if it has a Support>Support_Threshold set. If an Item-set is frequent (Support above Support Threshold), all its subsets are also frequent. Hence, we don’t need to calculate Support for each rule. <br/>
Ex: If Support {Milk, Cheeze, Eggs} is above the Support Threshold, then, {Milk, Cheeze}, {Cheeze, Eggs}, {Milk, Eggs}, etc.  also have their Support above threshold. Hence, a lot of comparisons saved.

![1](https://user-images.githubusercontent.com/81899253/137438042-eb1a4aac-5535-49ec-ae83-dcf6958afc6c.png) <br/>
In the above image, if ‘cde’(last greyed cell) is frequent, all the greyed item-sets are also frequent automatically <br/>

If an item-set A is infrequent, then all its super-sets (sets for which A is a subset) are also infrequent. Hence, if {Milk} is infrequent, {Milk, Eggs},{Milk, Cheeze, Eggs}, etc. all are infrequent & hence their Support shouldn’t be calculated. Again, saving comparisons.

![2](https://user-images.githubusercontent.com/81899253/137438318-fa382f35-003f-4399-a9f3-8a17d9af0aba.png) <br/>
If ‘ab’ is infrequent, every super-set is infrequent & can be ignored then & there.

**Algorithm in a nutshell**
1. Set a minimum support and confidence.
2. Take all the subset present in the transactions which have higher support than minimum support.
3. Take all the rules of these subsets which have higher confidence than minimum confidence.
4. Sort the rules by decreasing lift.

**Conclusion**  <br/>
This “Apriori Algorithm” is very useful tool in “Market Basket Analysis” such as- <br/>
Here, based on the analysis performed you could get to know the associations between the items so that the manager can take decisions accordingly. This analysis would help to know if certain groups of items are consistently purchased together and use this data for adjusting store layouts, cross-selling, promotions based on statistics. It will not only in arranging the items but also to attract the customer by keeping discounts on some items e.g. “If you buy big packet of Maggie then you will get 10% off on tea powder.” Also it would help the customer to get reminded to buy items or become convenient to pick up in near place.




