
In our system we have an OrderTrackingScreen that 
allows users to track their orders in real-time. We want to increase UX by adding new features and 
improving the interface in time tracking

We’re improving the UX in our OrderTrackingScreen.dart

so lets say we currenly have formatted ETA time like this:

///

Text(
  DateFormat('hh:mm a').format(widget.order.estimatedArrivalTime!),
  style: const TextStyle(
    fontSize: 18,
    fontWeight: FontWeight.w700,
    color: Colors.white,
  ),
),


////

Its not user friendly to show the ETA time in a static format. Instead,
we can enhance the user experience by displaying a dynamic countdown timer 
that updates in real-time. This way, users can easily see how much time is left until 
their order arrives without having to calculate it themselves.


so instead of just time , we can show something like this:
“Arriving in 12 mins” or 
“Arriving in 1 hr 5 mins”
“Arrived” (if the ETA is in the past)

So the function is given below 

String getArrivalMessage(DateTime? eta) {
  
  // TODO: Implement here

  return '';
}

///// 
so now Replace the ETA text widget to use your function. and Refactor this so it uses your getArrivalMessage() function instead




