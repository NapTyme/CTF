# Printer Shares

**Category:** General Skills  
**Points:** 50

### 1. Challenge Description

Someone accidentally sent an important file to a network printer. The challenge is to retrieve it from the print server running on port `51986`.

### 2. My Approach

- **Initial Thought:** Used the provided `nc -vz` command to verify the port was open and accepting TCP connections, confirming the service was live.
- **Research:** Recognised that "Printer Shares" hinted at SMB (Server Message Block) — the protocol used for sharing files and printers over a network. Used `smbclient` to enumerate available shares on the server anonymously.
- **Execution:** Listed the shares and found one called `shares`. Connected to it anonymously and listed the contents, finding `dummy.txt` (a decoy) and `flag.txt`. Downloaded `flag.txt` using `get`, exited the smbclient prompt, and read the flag with `cat`.

### 3. Commands Used

```
nc -vz mysterious-sea.picoctf.net 51986
smbclient -L mysterious-sea.picoctf.net -p 51986 -N
smbclient //mysterious-sea.picoctf.net/shares -p 51986 -N
ls
get flag.txt
exit
cat flag.txt
```
