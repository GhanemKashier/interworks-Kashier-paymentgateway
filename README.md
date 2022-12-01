
 this documentation can be divided into two main categories:
1.	Product 
2.	Process 
Product
Kashier has designed his gateway to be able to handle transaction submissions and responses in the .Net format.  If you would like to use the .Net interworks.cloud emulator then your shopping cart or application must support the .Net.
Kashier Gateway dll URL is:
          https://github.com/GhanemKashier/interworks-Kashier-paymentgateway
there are two dll file Iwcp.PaymentGateways.SetupOptions.Kashier.dll and Iwcp.PaymentGateways.Kashier.dll

•	Iwcp.PaymentGateways.SetupOptions.Kashier.dll 
                     provide configuration page to insert the MID, Api Key and paymentUrl 
        note “paymentUrl is https://kashier-orange.herokuapp.com/"
•	Iwcp.PaymentGateways.Kashier.dll
                     simply provide the transaction POST URL to Kashier Gateway URL
Process
  if you used interworks.cloud emulator  lightweight that enables you to load your code and debug it just like it was loaded in the Storefront but with the perks that come with a mocked environment, such as ease of deployment, short load times (no DB is needed, no activation, etc) and more, You will need to change something at  storage.json due of  no data base
1.	set the configuration setting at payment Gateways key like that
 
                                             Figure 1 payment Gateway setting
2.	 paymentMethodId at account object must equal id at paymentMethods array

       
                               Figure 2 paymentMethods id equal paymentMethods


3.	place Kashier .dll files inside the “bin” folder of Storefront 
4.	now you can run Storefront by Visual Studio with .net framework 4.8
 
                                                                            
5.	after run insert amount then submit (Figure 3)
 
6.	then you will redirect to Kashier payment gateway 
 
 
                                                                  

7.	Choose the payment method, either card or wallet
8.	Once paid, it directs you to the home page and inform you of the status of the transaction. 
  
                                                                                            
9.	then store this transaction at store.json or database 
   
                                            Figure 6 payment status and transaction details

 
 





