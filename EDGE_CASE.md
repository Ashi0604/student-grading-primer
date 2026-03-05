# Document your edge case here
- To get marks for this section you will need to explain to your tutor:
1) The edge case you identified
2) How you have accounted for this in your implementation

### Edge case identified
Creating a student without the required fields `name` or `course`.

### How it is handled
In the `/students` POST endpoint, the API checks if the request body contains both `name` and `course`. If either field is missing, the API returns a `404` error with the message `"Missing required fields"`.

### Reason
A student record must contain both a name and a course to be valid. Rejecting incomplete requests prevents invalid data from being inserted into the database.