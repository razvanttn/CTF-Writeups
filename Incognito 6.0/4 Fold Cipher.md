# Welcome – SSS CTF Challange Writeup

| Info        | Details            |
|-------------|--------------------|
| Category    | Crypto             |
| Points      | 50                 |

# Challenge Overview

> This crypto challange seems to be weird we look at it at first. The first thing I tried was concatenating all digits and removing `/` to get some binary text. Nothing happened.
![overview][https://i.imgur.com/2bMEGha.png]

## Given ciphertext
>00 0001 000 101 010 1001 / 011010 1000 01 000 0000 / 0000 010 / 0000 010 000 110 / 00001 01111 11 11111 111 1000 1011 00001 1011 / 0000 010 / 1 1100 111 001 / 0001 000 110

# Steps

## 1. Binary → Morse Code

I noticed a possible Morse pattern where `0 = "."` and `1 = "-"`. The `/` symbols separate words, just like in Morse. After converting:

```
.. ...- ... -.- .-. -..- / .--.-. -... .- ... .... / .... .-. / .... .-. ... --. / ....- .---- -- ----- --- -... -.-- ....- -.-- / .... .-. / - --.. --- ..- / ...- ... --.
```

Using a Morse translator, this gives:
```
IVSKRX@BASHHRHRSG41M0OBY4YHRTZOUVSG
```

## 2. Decrypt the String
![img1](https://hackmd.io/_uploads/SkcmCY0yxx.png)

By **Reversing** the string and applying the **Atbash Cipher**, the result becomes:

```
THEFLAGISB4BYL0N14THISISSHZY@CIPHER
```

# Final Flag

```
ictf{B4BYL0N14}
```
