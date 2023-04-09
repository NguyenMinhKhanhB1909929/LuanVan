## README

### Requires:
- Next.js
- TypeScript
- Antd
- Antd Form Builder
- Recoil
- i18n

### Spec:

This is a website for SS staff/admin to book a meeting room.

1. General:  

* Any user can view list booking request 

* Any user can view booking request in Calendar mode. 

* Once request status is created, an email will be automatically send  to: Admins. 

* Once request status changed to Reject/Approve, an email will be automatically send  to: its Creator. 

2. Staff:  (same as Users TOPIC 1) 

* Any staff can create a booking request. Once booking request is created, its status will be: 

  * Pending: startDate of the request must be after today. On a pending request, Request creator can: (1) Update  startDate-endDate, room; (2) Reject this request. 
  * Reject: if Admin manually reject any request OR request's endDate pass today (like out-dated request). 
  * Otherwise Approve, if Admin manually approve request  

3. Admin:  

* Admin can do an action on a request: Reject/Approve. This action is irrevertible. 

* Admin can manage rooms: CRUD 

4. Entities: 

a. Booking request:

* StartTime - EndTime (required): The time staff want to book a room 
=> or StartTime – duration (InputNumber: mins) (validate overlap booking – BE) 

* Reason (optional) 

* Room (required): the room want to book (select from available room) 

b. Request status (Pending, Approve, Reject) 

c. Room (entity):  
* Name 

* ID 

* Capacity (small/big room) 