I am using Target.com 
Test Model

Test Case ID: PickUp1
Integration Test
Description: Check in-store pickup location finder when not signed into an account
Preconditions: Browser capable of supporting the site. Device has location services turned on. 
Test Steps: 
    1.) go to Target.com 
    2.) choose **Pickup & Delivery**
    3.) Drop down menu select Shop Order Pickup 
    4.) Confirm that “In-store pickup at <store closest to your location>” displays 
Expected Result: Even when not signed into an account, the store finder should find a store within your area that is available for in-store pickup 

Test Case ID: PickUp2
Functionality Test
Description: Check in-store pickup location finder when not signed into an account and location services disabled
Preconditions: Browser capable of supporting the site. 
Test Steps: 1.) go to Target.com 
2.) choose Pickup & Delivery
3.) Drop down menu select Shop Order Pickup 
Expected Result: Pop-up should read “For better results, please turn on location services on your device and reload page. Or please select Store Finder in the menu.” 

Test Case ID: PickUp3 
Critical Path Test 
Description: Check in-store pickup location finder when not signed into an account and location services disabled
Preconditions: Browser capable of supporting the site. 
Test Steps: 1.) go to Target.com 
2.) choose Pickup & Delivery
3.) Drop down menu select Shop Order Pickup 
4.) From the pop-up select Store Finder
Expected Result: The user should be taken to Store Finder page where they have the option to enter a zip code or city and state

Test Case ID: PickUp4
User Interface Test
Description: Check in-store pickup location finder, when logged into an account
Preconditions: Browser capable of supporting the site. Location services turned on device. Logged into account
Test Steps: 1.) choose Pickup & Delivery 
2.) Drop down menu select Shop Order Pickup
3.) Confirm your home store is correct location 
Expected Result: Banner should read “Welcome to your home store <store location>! Pickup today,<user name>!”

Test Case ID: PickUp5 
Boundary Value Analysis
Description: When logged into account and choosing a pickup location that is more than 25 miles away from home store.  
Preconditions: Browser capable of supporting the site. Location services turned on device. Logged into account. Have an item in your shopping cart.
Test Steps: 1.) Click on shopping cart icon
2.) Choose Select a Different Pickup Location 
3.) Select a store that is 26 miles or more from your home store 
Expected Result: A warning should pop up that reads “Are you sure you want to choose <store name>?” 


Test Case ID: PickUp6 
Boundary Value Analysis
Description: When logged into account, and choosing a pickup location that is 25 miles away from home store.  
Preconditions: Browser capable of supporting the site. Location services turned on device. Logged into account. Have an item in your shopping cart.
Test Steps: 1.) Click on shopping cart icon
2.) Choose Select a Different Pickup Location 
3.) Select a store that is 25 miles from your home store 
Expected Result: A warning should pop up that reads “Your <home store> also has this item available for pick-up. Are you sure you want to pickup at <store name>?”

Test Case ID: PickUp7 
Boundary Value Analysis
Description: When logged into account, and choosing a pickup location that is less than 25 miles away from home store.  
Preconditions: Browser capable of supporting the site. Location services turned on device. Logged into account. Have an item in your shopping cart.
Test Steps: 1.) Click on shopping cart icon
2.) Choose Select a Different Pickup Location 
3.) Select a store that is 2 miles from your home store 
Expected Result: A warning should pop up that reads “Your <home store> also has this item available for pick-up. Are you sure you want to pickup at <store name>?”


Test Case ID: PickUp8 
Integration Test 
Description: What happens when an item is out-of-stock at home store. 
Preconditions: Browser capable of supporting the site. Location services turned on device. Logged into account. Have an item in your shopping cart that is not available at home store. 
Test Steps: 1.) Click on shopping cart icon
Expected Result: Beneath item photo, home store should be grayed out. “Check other stores?” should display. 

Test Case ID: PickUp9
Integration Test 
Description: Check other stores for item in shopping cart when not logged into an account.
Preconditions: Browser capable of supporting the site. Location services turned on device. Have an item in your shopping cart that is unavailable at the current store you have selected.
Test Steps: 1.)Click on shopping cart icon
2.) Select Check Other Store option 
Expected Result: Pop-up should contain a list of stores that have the item in stock within a 25 mile radius of the user.

Test Case ID: PickUp10
Error Test 
Description: When an item is only available for home delivery.
Preconditions: Browser capable of supporting the site.  Have an item in your shopping cart that is not available for in-store pickup. 
Test Steps: 1.)Click on shopping cart icon 
2.) Select Check Other Store option
Expected Result: Pop-up that reads “We’re sorry this item is only available for home delivery. Please login to your account or select Checkout as Guest.” 



