# Bytemancy 0

**Category:** General Skills  
**Points:** 50

### 1. Challenge Description

Upon launching the instance, a netcat command is provided to connect to a remote service. The service prompts you to send specific ASCII decimal values side-by-side with no spaces.

### 2. My Approach

- **Initial Thought:** Connected to the service using the provided `nc` command, which presented the BYTEMANCY 0 challenge asking to send ASCII DECIMAL 101 101 101 side-by-side with no space.
- **Research:** Looked up ASCII decimal value 101, which corresponds to the character `e`.
- **Execution:** Sent `eee` (three instances of `e` with no spaces) back to the service, which returned the flag.

### 3. Commands Used

```
nc candy-mountain.picoctf.net 58240
eee
```
