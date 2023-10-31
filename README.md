# A/B Testing For E-commerse Website

A/B testing helps in finding a better approach to finding customers, marketing products, getting a higher reach, or anything that helps a business convert most of its target customers into actual customers.

#   Background

A E-commerce company wants to find out the best campaign for the company to get more customers.
Two campaigns were performed by the company:
* Control Campaign
* Test Campaign

#   Dataset

 * The dataset contains two data files about two marketing campaigns (Control Campaign and Test Campaign).
 * [Dataset source: Kaggle](http://kaggle.com/)
 * Below are all the features in the dataset:

      1. Campaign Name: The name of the campaign
      2. Date: Date of the record
      3. Spend: Amount spent on the campaign in dollars
      4. of Impressions: Number of impressions the ad crossed through the campaign
      5. Reach: The number of unique impressions received in the ad
      6. of Website Clicks: Number of website clicks received through the ads
      7. of Searches: Number of users who performed searches on the website 
      8. of View Content: Number of users who viewed content and products on the website
      9. of Add to Cart: Number of users who added products to the cart
      10. of Purchase: Number of purchases

#   Data Preprocessing

* Checking NULL Values and filling with mean value

```
1. print(control_data.isnull().sum())
2. control_data["Reach"].fillna(value=control_data["Reach"] \  .mean(),inplace=True)
```

* Merging the dataset
```
ab_data = control_data.merge(test_data, how="outer").sort_values(["Date"])
ab_data = ab_data.reset_index(drop=True)
print(ab_data.head())
```

# A/B Testing to Find the Best Marketing Strategy

* Analyze the relationship between the number of impressions.<br/>
        [Dataset source: Kaggle](http://kaggle.com/)<br/>
        ```
        The control campaign resulted in more impressions according to the amount spent on both campaigns.
        ```


* The number of searches performed on the website from both campaigns:<br/>
         [Dataset source: Kaggle](http://kaggle.com/)<br/>
         ```
        The test campaign resulted in more searches on the website.
        ```
* The number of website clicks from both campaigns:<br/>
         [Dataset source: Kaggle](http://kaggle.com/)<br/>
         ```
        The test campaign wins in the number of website clicks. 
        ```
* The amount of content viewed after reaching the website from both campaigns:<br/>
         [Dataset source: Kaggle](http://kaggle.com/)<br/>
         ```
        The audience of the control campaign viewed more content than the test campaign.
        Its engagement on the website is higher than the test campaign.
        ```
* The number of products added to the cart from both campaigns:<br/>
         [Dataset source: Kaggle](http://kaggle.com/)<br/>
         ```
        Despite low website clicks more products were added to the cart from the control campaign.
        ```
* The amount spent on both campaigns:<br/>
         [Dataset source: Kaggle](http://kaggle.com/)<br/>
         ```
        The amount spent on the test campaign is higher than the control campaign.But the control campaign resulted in more content views
        and more products in the cart, the control campaign is more efficient than the test campaign.
        ```
* The purchases made by both campaigns:<br/>
         [Dataset source: Kaggle](http://kaggle.com/)<br/>
         ```
        There’s only a difference of around 1% in the purchases made from both ad campaigns.
        Control campaign resulted in more sales in less amount spent on marketing,So the control campaign is better then test campaign here.
        ```
* The relationship between the number of website clicks and content viewed from both campaigns:<br/>
         [Dataset source: Kaggle](http://kaggle.com/)<br/>
         ```
        The website clicks are higher in the test campaign, but the engagement from website clicks is higher in the control campaign. So the control campaign wins!
        ```
* Analyze the relationship between the amount of content viewed and the number of products added to the cart from both campaigns:<br/>
         [Dataset source: Kaggle](http://kaggle.com/)<br/>
         ```
         The control campaign wins!
        ```
* The relationship between the number of products added to the cart and the number of sales from both campaigns:<br/>
         [Dataset source: Kaggle](http://kaggle.com/)<br/>
         ```
         The control campaign resulted in more sales and more products in the cart,but the conversation rate of the test campaign is higher.
        ```

# Summery

From the above A/B tests, we found
* The control campaign resulted in more sales and engagement from the visitors. More products were viewed from the control campaign, resulting in more products in the cart and more sales.
* The conversation rate of products in the cart is higher in the test campaign.
* The test campaign resulted in more sales according to the products viewed and added to the cart. And the control campaign results in more sales overall.
* The Test campaign can be used to market a specific product to a specific audience, and the Control campaign can be used to market multiple products to a wider audience.


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Thanks to @Aman Kharwal for valuable guidence

       
  
