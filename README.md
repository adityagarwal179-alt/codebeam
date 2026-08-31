# Codebeam

One-time code se file, photo, video ya text seedha ek browser se doosre tak bhejo — peer-to-peer (WebRTC), koi server par file store nahi hoti.

## Kaise chalayein

**Option A — Sirf apne liye / local testing**
`index.html` ko double-click karke seedha browser me khol lo. Kaam karega, lekin doosre insaan ko bhi yahi file bhejni padegi aur unhe bhi apne computer par khol ke rakhni hogi.

**Option B — GitHub Pages (recommended)**
Isse ek hi link ban jaata hai jo dono log apne-apne browser me khol sakte hain — file bhejne ki zaroorat nahi.

1. GitHub par ek naya repository banao (e.g. `codebeam`)
2. Is `index.html` ko us repo ke **root** me upload karo (folder ke andar nahi — seedha root me)
3. Repo ke **Settings → Pages** me jao
4. **Source**: "Deploy from a branch" → Branch: `main` → Folder: `/ (root)` → **Save**
5. ~30–60 second baad link milega: `https://<tumhara-username>.github.io/codebeam/`
6. Yahi link dono devices par kholo — sender code banayega, receiver wahi code daalega

## Folder structure

```
codebeam/
├── index.html   ← yahi file, root me
└── README.md
```
Bas itna hi chahiye — koi build step, koi backend, koi database nahi.

## Ye kaam kaise karta hai

- Connection jodne ("signaling") ke liye PeerJS ki free public cloud service use hoti hai
- Ek baar connection ban jaaye, actual file transfer **seedha do browsers ke beech** hota hai — kisi server se hokar nahi guzarta
- Isliye dono taraf ka internet chalna zaroori hai, aur transfer poora hone tak dono tabs khule rehne chahiye
