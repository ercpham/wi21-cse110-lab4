## DevTools - Debugging

### What was the bug?
We expect to add two numbers, but we end up appending a string to another one.

### How would you fix it?

Cast the numbers in the adding function to numbers by using parseInt().

## DevTools - Network Tab
1. What is the name of the new json file?

    citylots.json

2. Which file initiated the download of the new file?

    part2.js

3. What is its file size?

    11.7 MB

4. How long did it take to download?

    90ms


Next, select the file to bring up a new side panel to answer the following:

5. What was your User-Agent for the browser that made the request?

    Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.141 Safari/537.36

6. In the response, what type of server did it come from?

    Apache

7. When was the file last modified?

    Tue, 26 Jan 2021 22:14:13 GMT

8. What was the Content-Type of the file?

    application/json


Navigate to the Initiator tab now and answer the last question

9. Which method inside the initiating file made the request?

    fetchData
