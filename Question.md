# Order Tracking Screen UX Improvement

In our system, we have an **OrderTrackingScreen** that allows users to track their orders in real-time. We want to increase UX by adding new features and improving the interface in time tracking.

We’re improving the UX in our `OrderTrackingScreen.dart`.

Currently, the ETA time is formatted like this:

```dart
Text(
  DateFormat('hh:mm a').format(widget.order.estimatedArrivalTime!),
  style: const TextStyle(
    fontSize: 18,
    fontWeight: FontWeight.w700,
    color: Colors.white,
  ),
)
```

It's not user friendly to show the ETA time in a static format. Instead, we can enhance the user experience by displaying a dynamic countdown timer that updates in real-time. This way, users can easily see how much time is left until their order arrives without having to calculate it themselves.

## Requirements

Implement the function below to generate a user-friendly arrival message based on the ETA:

- If `eta` is `null`, return an empty string (no ETA available).
- If the ETA is in the past (i.e., `eta` is before `DateTime.now()`), return `'Arrived'`.
- Otherwise, return a countdown like `'Arriving in 1 hr 5 mins'` or `'Arriving in 12 mins'`.
- Use `DateTime.now()` to calculate the difference.
- Show hours and minutes as appropriate (omit hours if less than 1 hour).

## Output Examples

| Current Time        | ETA                 | Output                  |
| ------------------- | ------------------- | ----------------------- |
| 2026-02-13 12:00:00 | 2026-02-13 12:12:00 | Arriving in 12 mins     |
| 2026-02-13 12:00:00 | 2026-02-13 13:05:00 | Arriving in 1 hr 5 mins |
| 2026-02-13 12:00:00 | 2026-02-13 11:59:00 | Arrived                 |
| 2026-02-13 12:00:00 | null                |                         |

The function is given below:

```dart
String getArrivalMessage(DateTime? eta) {
  // TODO: Implement here

  return '';
}

/////
so now Replace the ETA text widget to use your function. and Refactor this so it uses your getArrivalMessage() function instead




```
