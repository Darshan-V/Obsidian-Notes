### Info.
- [/] Edit seats and hours on the Booking screen -> method to edit direct input or modal?
- [x] About payment method on the booking screen
- [b] why auth on payment
- [x] TODO Booking confirmation screen when and where to show other than after payment
- [x] Link share screen -> might be getting data from the api
- [x] Is share for booking required in the profile/bookings
- [x] where is the data for the gaming cafe being fetched on the first screen

### Todos
 - [x] Booking screen  
 - [x] Shared screen and form confirmation 
 - [x] Shared/Friends screen confirmation 
 - [x] Profile screen 
 - [x] My bookings
 - [x] Wallet
 - [x] My account
 - [x] On profile/account what's the edit method?
 - [x] Fix header on profile sub routes
 - [x] Bookings sub -> payment and auth
 - [x] user booking confirmation
 - [x] recharge my wallet flow
 - [x] why is wallet topup wrt. cafes
 - [ ] remove userToken param from the getClientSlots


## Mappings
App context {common app data} -> Login Context{Auth, token, secret, path(persist user token)} -> Booking Context {seats, hours, selected date, selected timings, server id (non persistent)} -> Wallet Context {custom amount / selected amount, mode of payment (non persistent)}

### API integration
- [x] previewUser
- [ ] getClientSlots
- [x] getUser
- [x] getUserToken
- [ ] payment -> pg -> postBooking
- [x] userVerification
- [x] login
- [ ] registerServerClient
- [ ] updateUser
- [x] getClientSessions
- [ ] wallet recharge amount listing
- [ ] coupon list


