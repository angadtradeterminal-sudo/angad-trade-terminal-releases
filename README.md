# AngadTradeTerminal — release channel

Yeh repo **sirf update baantne ke liye** hai. App ka source code yahan nahi hai.

Ismein do cheezein rehti hain:

| | |
|---|---|
| `latest.json` | signed manifest — naya version kaun sa hai, uski zip kahan hai, aur uska SHA-256 |
| Releases → asset | `AngadTradeTerminal-<version>.zip` — pehle se compiled app |

App khud har baar shuru hote waqt `latest.json` padhti hai, uski signature aur zip
ka SHA-256 jaanchti hai, aur tabhi naya version lagati hai. Signature galat ho,
hash na mile, ya version purana ho — to kuch nahi badalta, app purane version se
hi chal padti hai.

Zip yahan khuli padi hai, par usse kisi ka kuch nahi banta: app **licensed
machine** par hi chalti hai. Bina issue ki hui license ke wo start hi nahi hoti.

---

**This repo only distributes updates.** No source code here — just a signed
manifest (`latest.json`) and the compiled app zip as a release asset. The app
verifies the manifest signature and the zip's SHA-256 before applying anything,
and refuses to run at all without a license issued for that machine.
