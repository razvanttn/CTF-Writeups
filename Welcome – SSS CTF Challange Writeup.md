# 🛡️ Welcome – SSS CTF Challange Writeup

| Info        | Details            |
|-------------|--------------------|
| Category    | Web Exploitation    |
| Difficulty  | Easy                |


#  Challenge Overview

> This challange hides a flag splitted in 4 parts, as we're being told in the home


#  Steps

## 1. Inspecting Page Source

- Line 4: `/static/css/main.css` → `FFF{rirel_`
- Lines 14-15: found `svyr_`
- Line 21: `/static/hidden.js?v=` → `unf_`
- `/static/logo.png` → `srryvatf}`

## 2. Rebuilding the Flag
Concatenated: FFF{rirel_svyr_unf_srryvatf}
> ROT13 to it and obtain the flag: SSS{every_file_has_feelings}

