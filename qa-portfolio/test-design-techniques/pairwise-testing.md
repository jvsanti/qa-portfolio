# Test Design: Pairwise Testing — Conduit Compatibility Matrix

5 parameters (Resolution, Browser, OS, Language, Connection speed) with multiple values each — full combinatorial coverage would require hundreds of test cases. Pairwise reduced this to **10 test cases** while still covering every pair of values at least once.

| # | Resolution | Browser | OS | Language | Connection speed |
|---|---|---|---|---|---|
| 1 | 1920x1080 | Chrome | Windows 10 | English | Fast (Wi-Fi/4G) |
| 2 | 1366x768 | Firefox | macOS | Portuguese | Fast (Wi-Fi/4G) |
| 3 | 360x640 | Safari | Linux | Spanish | Fast (Wi-Fi/4G) |
| 4 | 360x640 | Edge | Android | Portuguese | Slow (3G) |
| 5 | 1366x768 | Edge | Windows 10 | Spanish | Slow (3G) |
| 6 | 1920x1080 | Safari | Android | English | Slow (3G) |
| 7 | 1920x1080 | Firefox | Linux | Spanish | Slow (3G) |
| 8 | 1366x768 | Chrome | Linux | Portuguese | Slow (3G) |
| 9 | 360x640 | Chrome | macOS | Spanish | Slow (3G) |
| 10 | 360x640 | Firefox | Windows 10 | English | Slow (3G) |
