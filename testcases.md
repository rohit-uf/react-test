# Testcases


## Sample Teacher Availability

```json
[
  {
    "weekday": "monday",
    "slots": [
      { "start_time": "9 AM", "end_time": "10 AM" },
      { "start_time": "11 AM", "end_time": "12 PM" },
      { "start_time": "3 PM", "end_time": "4 PM" }
    ]
  },
  {
    "weekday": "wednesday",
    "slots" : [
      { "start_time": "9 AM", "end_time": "10 AM" },
      { "start_time": "10 AM", "end_time": "11 AM" },
      { "start_time": "11 AM", "end_time": "12 PM" },
      { "start_time": "1 PM", "end_time": "2 PM" },
      { "start_time": "2 PM", "end_time": "3 PM" }
    ]
  },
  {
    "weekday": "friday",
    "slots": [
      { "start_time": "9 AM", "end_time": "10 AM" },
      { "start_time": "10 AM", "end_time": "11 PM" },
      { "start_time": "11 AM", "end_time": "12 PM" },
      { "start_time": "12 PM", "end_time": "1 PM" },
      { "start_time": "1 PM", "end_time": "2 PM" }
    ]
  }
]

```

## Sample Student Requests and Response

```js

// Request 1

{
  "student_name": "Shantanu Arora",
  "preferences": [
    {
      "weekday": "monday",
      "start_time": "9 AM",
      "end_time": "10 AM"
    },
    {
      "weekday": "monday",
      "start_time": "10 AM",
      "end_time": "11 AM"
    },
    {
      "weekday": "friday",
      "start_time": "1 PM",
      "end_time": "2 PM"
    },
}

// Response Success

{
  "confirmed": true,
  "weekday": "monday",
  "start_time": "9 AM",
  "end_time": "10 AM",
  "date": "1 August 2022"
}

// Response Failure

{
  "confirmed": false,
  "reason": "teacher is not available on any of your preferred days"
}

```

