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
- [x] registerServerClient
- [x] updateUser
- [x] getClientSessions
- [ ] wallet recharge amount listing
- [x] coupon list
- [x] inituserserverwallet
- [x] rechargewallet
- [x] pending balance wallet -> GetUserServerWalletApi
- [x] remove input from the apply coupon -> add skip button
- [ ] initPayment->razorpaypopup-> recharge wallet(razorpay signature).
- [ ] input/select-> coupon[if no coupon navigate next]->summary[pay button(initrazorpay)]
- [ ] share url ?
- [ ] require api to show order summary before payment -> use initPayment
- [!] wallet // -> do login check before navigating to the recharge my wallet
- [ ] onpay button -> call only razorpay api
- [ ] getServerWallets(list of wallets)
- [ ] getserversessions->initi
- [ ] base amount, gst & servercharges, platform fees
## Clean up
- [ ] keep only token, serverID in the context -> root context-> session storage
## Routes
-> home /id
-> /bookings -> all booking data
-> on success payment navigate to bookings -> share button only if there are unclaimed component
-> Remove option to edit phone -> getUserApi -> updateUserApi -> update user name