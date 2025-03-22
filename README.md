# Evershop_API_Testing

## Overview
This repository contains a Postman collection for testing the Evershop API. The collection includes various API requests to search for products, select a specific item, add it to the cart, and view the cart.

## Prerequisites
- [Postman](https://www.postman.com/downloads/)
- A valid internet connection

## Installation
1. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/Evershop_API_testing.git
   ```
2. Open Postman and import the `Evershop_API_testing.postman_collection.json` file.

## Collection Details
This collection contains the following requests:

1. **Search Shoe**  
   - Method: `GET`  
   - URL: `{{base_url}}/search?keyword=Nike+react+phantom+run+flyknit+2&ajax=true`  
   - Purpose: Searches for a specific shoe model.

2. **Click on the Shoe**  
   - Method: `GET`  
   - URL: `{{base_url}}/men/nike-react-phantom-run-flyknit-2-180?size=25&color=14&ajax=true`  
   - Purpose: Simulates clicking on a selected shoe product.

3. **Small Size Black Shoe**  
   - Method: `GET`  
   - URL: `{{base_url}}/men/nike-react-phantom-run-flyknit-2-180?size=25&color=14&ajax=true`  
   - Purpose: Fetches details for a black shoe of size small.

4. **Add to Cart**  
   - Method: `POST`  
   - URL: `{{base_url}}/cart/items`  
   - Body:
     ```json
     {
       "sku": "NJC48508-Black-S",
       "qty": "2"
     }
     ```  
   - Purpose: Adds the selected shoe to the cart.

5. **View Cart**  
   - Method: `GET`  
   - URL: `{{base_url}}/cart`  
   - Purpose: Retrieves the current cart details.

## Environment Variables
The collection uses the following variable:
- `base_url`: `https://demo.evershop.io/`

## Running Tests
1. Open Postman and navigate to the **Evershop API Testing** collection.
2. Select a request and click **Send** to execute.
3. Observe the response data to verify the expected results.

