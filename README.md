# android-candidate-test
Coding challenge for android candidates applying to Retailio.

# Tasks:
## Design an app for placing order:
1. Load the medicines and list of retailers from the given API and store locally.
2. Show the list of retailers and allow user to select one.
3. Selecting a retailer should open the list of medicines with search functionality.
4. Allow multi-select and Search functions for medicines (Everything locally no API calls).
5. Allow user to select as many medicines in as much quantity he/she wants; if user selects same medicine twice create a single    entry and increase the quantity.
6. Provide a button for placing the order after selecting medicines with given API. If internet is not available maintain a        queue of orders, and whenever internet connection is established, place the order automatically even if the app is not in      foreground. Please ensure that one order should not be placed multiple times.
7. Manage the orientation changes.
8. Assume your own UI, feel free to use libraries, make sure app doesn’t crash.
9. Upload the code to GitHub or anywhere publicly so that we can review it.

## Enhancement (Optional) :
Create a view which will list all the orders which are not synced with server.Show a loader with the order entry which is under the process of syncing indicating that it is currently syncing with server.

## APIs:
### GET Retailers:
```
curl -i -H "Accept: application/json" -H "Content-Type: application/json" -X GET https://retailio-api-test.herokuapp.com/test/api/retailers
```
### GET Medicines:
```
curl -i -H "Accept: application/json" -H "Content-Type: application/json" -X GET https://retailio-api-test.herokuapp.com/test/api/medicines
```
### POST Place Order:
```
curl -i -H "Content-Type: application/json" -X POST -d '[{"product_id":12, "quantity":1}]' https://retailio-api-test.herokuapp.com/test/api/placeOrder
```
