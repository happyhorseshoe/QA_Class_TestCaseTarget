I am using Target.com 
Test Model

## Test Case ID: PickUp1 <br>
Integration Test<br>

>Description: Check in-store pickup location finder when not signed into an account<br>

Preconditions: Browser capable of supporting the site. Device has location services turned on. <br>

Test Steps: 
1. go to Target.com 
2. choose **Pickup & Delivery**
3. Drop down menu select **Shop Order Pickup** 
4. Confirm that “In-store pickup at (*store closest to your location*)” displays <br>

 Expected Result: Even when not signed into an account, the store finder should find a store within your area that is available for in-store pickup    
<br>

## Test Case ID: PickUp2 <br>

Functionality Test<br>

>Description: Check in-store pickup location finder when not signed into an account and location services disabled<br>

Preconditions: Browser capable of supporting the site. <br>

Test Steps: 
1. go to Target.com 
2. choose **Pickup & Delivery**
3. Drop down menu select **Shop Order Pickup** <br>  
   
Expected Result: Pop-up should read “For better results, please turn on location services on your device and reload page. Or please select **Store Finder** in the menu.” 

<br>

## Test Case ID: PickUp3 <br>
Critical Path Test <br>

>Description: Check in-store pickup location finder when not signed into an account and location services disabled<br>

Preconditions: Browser capable of supporting the site. <br>

Test Steps:
1. go to Target.com 
2. choose **Pickup & Delivery**
3. Drop down menu select **Shop Order Pickup** <br>
4. From the pop-up select **Store Finder** <br>
   
Expected Result: The user should be taken to **Store Finder** page where they have the option to enter a zip code or city and state

<br>

## Test Case ID: PickUp4 <br>
User Interface Test <br>

>Description: Check in-store pickup location finder, when logged into an account<br>

Preconditions: Browser capable of supporting the site. Device has location services turned on.  Logged into account <br>

Test Steps:
1. choose **Pickup & Delivery** 
2. Drop down menu select **Shop Order Pickup**
3. Confirm your home store is correct location  <br>
   
Expected Result: Banner should read “Welcome to your home store (*store location*)! Pickup today, (*user name*)!”

<br>

## Test Case ID: PickUp5  <br>

Boundary Value Analysis <br>

>Description: When logged into account and choosing a pickup location that is more than 25 miles away from home store.  <br>

Preconditions: Browser capable of supporting the site. Device has location services turned on.  Logged into account. Have an item in your shopping cart.<br>

Test Steps: 
1. Click on shopping cart icon
2. Choose **Select a Different Pickup Location** 
3. Select a store that is 26 miles or more from your home store  <br>
   
Expected Result: A warning should pop up that reads “Are you sure you want to choose (*store name*)?” 

<br>


## Test Case ID: PickUp6  <br>

Boundary Value Analysis <br>

>Description: When logged into account, and choosing a pickup location that is 25 miles away from home store.  <br>

Preconditions: Browser capable of supporting the site. Device has location services turned on.  Logged into account. Have an item in your shopping cart.<br>

Test Steps: 
1. Click on shopping cart icon
2. Choose **Select a Different Pickup Location**
3. Select a store that is 25 miles from your home store 
   
Expected Result: A warning should pop up that reads “Your (*home store*) also has this item available for pick-up. Are you sure you want to pickup at (*store name*)?”

<br>

## Test Case ID: PickUp7 <br>

Boundary Value Analysis <br>

>Description: When logged into account, and choosing a pickup location that is less than 25 miles away from home store.  <br>

Preconditions: Browser capable of supporting the site.  Device has location services turned on.  Logged into account. Have an item in your shopping cart. <br>

Test Steps: 
1. Click on shopping cart icon
2. Choose **Select a Different Pickup Location** 
3. Select a store that is 2 miles from your home store 
   
Expected Result: A warning should pop up that reads “Your (*home store*) also has this item available for pick-up. Are you sure you want to pickup at (*store name*)?”

<br>

## Test Case ID: PickUp8 <br>

Integration Test  <br>

>Description: What happens when an item is out-of-stock at home store. <br>

Preconditions: Browser capable of supporting the site. Device has location services turned on. Logged into account. Have an item in your shopping cart that is not available at home store. <br>

Test Steps: 
1. Click on shopping cart icon
   
Expected Result: Beneath item photo, home store should be grayed out. “**Check other stores**?” should display. 

<br>

## Test Case ID: PickUp9 <br>

Integration Test <br>

>Description: Check other stores for item in shopping cart when not logged into an account. <br>

Preconditions: Browser capable of supporting the site. Device has location services turned on.  Have an item in your shopping cart that is unavailable at the current store you have selected. <br>

Test Steps: 
1. Click on shopping cart icon
2.  Select **Check Other Stores** option 
   
Expected Result: Pop-up should contain a list of stores that have the item in stock within a 25 mile radius of the user.

<br>

## Test Case ID: PickUp10 <br>

Error Test <br>

>Description: When an item is only available for home delivery. <br>

Preconditions: Browser capable of supporting the site.  Have an item in your shopping cart that is not available for in-store pickup. <br>

Test Steps: 
1. Click on shopping cart icon 
2. Select **Check Other Stores** option
   
Expected Result: Pop-up that reads “We’re sorry this item is only available for home delivery. Please login to your **account** or select **Checkout as Guest**.” 



