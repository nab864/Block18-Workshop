# Unit Tests

## Multiplication

- Expect multiplication(2, 5) to be a number
- Expect multiplication(2, 5) to be a 10
- Expect multiplication(2, "g") to be an error
- Expect multiplication(-2, 5) to be a -10
- Expect multiplication(-2, -5) to be a 10
- Expect multiplication(2, 0.5) to be a 1
- Expect multiplication(2, "5") to be a 10

## concatOdds

-Expect concatOdds([2, 4, 1, 3, 9], [-1, 13, 7]) to be [-1, 1, 3, 7, 9, 13]
-Expect concatOdds([2, 4, 1, 3, 9], [-1, 13, 7, 3, 9]) to be [-1, 1, 3, 7 ,13]
-Expect concatOdds([2, 4, "1", 3, 9], [-1, 13, 7, 3, 9]) to be [-1, 3, 7 ,13]
-Expect concatOdds([2, 4, 1, 3, 9], [-1, 13, 7, 3, 9], [11, -3, 5]) to be [-1, 1, 3, 7 ,13]


# Functional Tests

## shoppingCart

- When the user clicks "checkout" with an empty cart, they should be shown an "empty cart" error and asked to add items to the cart
- When the user clicks "checkout" while not signed in, they should be given the option to create an account or check out as guest
- When the user clicks "checkout" while not signed in and chooses to checkout as guest, they should be shown a form to fill out their basic information: first name, last name, shipping address, email address
- When the user submits the guest form with an empty form entry, they should be shown an error and asked to fill out the missing entry
- When the user submits the guest form, they should be taken to the payment page
- When the user clicks "checkout" while signed in, they should be taken to the payment page
- When the user, on the Payment page, clicks "add payment" with an empty form entry, they should be shown an error and asked to fill out the missing entry
- When the user, on the Payment page, clicks "add payment" and the card info was incorrect, they should be shown an error and asked to input a valid card information
- When the user, on the Payment page, clicks "add payment" with all entries filled in and a valid card was used, they should be taken to the Verify Order page
- When the user, on the Verify Order page, clicks "place order", they should be shown a message saying "order complete" and then redirect to the Receipt page
- When the user, on the Verify Order page, clicks "place order", they should be sent an email with their receipt
