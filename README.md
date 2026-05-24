# HTTP Cleartext Form Submission Analysis with Wireshark

This mini-project demonstrates how HTTP form submissions can expose submitted data in cleartext when encryption is not used. I used Wireshark to capture a controlled login request sent to an intentionally vulnerable HTTP test site using dummy credentials.

The goal was to build hands-on familiarity with packet capture, HTTP traffic inspection, and privacy-aware security documentation.

## Tools Used

- Wireshark
- Web browser
- Intentionally vulnerable HTTP test site
- Dummy credentials for controlled testing

## What I Did

I started a Wireshark capture on my own machine, visited an intentionally vulnerable HTTP login page, and submitted fake login credentials.

I then filtered the capture using:

```text
http.request.method == "POST"
```

### Observation
In the packet details, Wireshark showed the submitted form fields in cleartext. The captured HTTP form data included the fields:
  uid
  passw
  btnSubmit
This demonstrates that HTTP does not encrypt submitted form data. If sensitive information is submitted over HTTP, it may be visible in packet captures.


