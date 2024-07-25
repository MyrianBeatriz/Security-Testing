# Understanding Race Conditions Cheatsheet

## What are Race Conditions?

Race conditions are vulnerabilities where concurrent requests interact with shared data simultaneously, leading to unintended behavior due to timing issues.

- **Scenario**: Multiple threads/processes access the same data concurrently.
- **Impact**: Can cause data corruption, security vulnerabilities, or application crashes.

## Types of Race Conditions

### Limit Overrun Race Conditions

- **Description**: Exploits application logic that allows exceeding predefined limits.
- **Example**: Redeeming a single-use gift card multiple times.

### How Race Conditions Work

- **Race Window**: Brief moment where collisions can occur due to processing timing.
- **Exploitation**: Timed requests intentionally cause collisions to exploit unintended behavior.

## Detection and Exploitation

### Methodology

1. **Identify Target Endpoint**:
   - Choose a rate-limited or single-use functionality.

2. **Issue Concurrent Requests**:
   - Use tools like Burp Suite's Repeater to send multiple requests in quick succession.

3. **Exploit Race Window**:
   - Align requests to overlap during the vulnerable race window.
   - Example: Repeatedly applying a discount code before it updates in the database.

### Tools

- **Burp Suite**: Utilize Burp Repeater with new features for HTTP/1 and HTTP/2 to minimize network jitter and maximize request synchronization.

