# Welcome to `Xtools UI` `v1.0.0` `(BETA)`

This guide will walk you through the setup process, from zero to a fully working tool.

---

## Table of Contents

1. [Getting the Requirements Ready](#1---getting-the-requirements-ready)
2. [Setting Up Proxies](#2---setting-up-proxies)
3. [Setting Up a CAPTCHA Solver](#3---setting-up-a-captcha-solver)
4. [Results & Output](#4---results--output)
5. [Advanced / Custom Output](#advanced--custom-output)
6. [Supported Tools & Output Formats](#supported-tools--output-formats)

---

## 1 - Getting the Requirements Ready

Our top priority is protecting users from accidental leaks that could lead to infections or unwanted bans. Therefore, Xtools requires **two essential elements**:

1. **Proxies**
2. **Solver credits**

These resources can be found on the home page.

![Home button](https://i.imgur.com/pcBpW4x.png)

![Sponsors](https://i.imgur.com/IUK28Dc.png)

---

## 2 - Setting Up Proxies

SOCKS5 proxies with **QUIC (HTTP/3) support** offer higher success rates against detection. They provide:

* Sticky sessions lasting **2–5 minutes**
* Support for **any region** *(note: cookies are region-locked)*
* Better reliability compared to single-IP proxies

It is strongly recommended to purchase **bandwidth-based proxy plans** rather than individual IP proxies. Bandwidth plans give you access to large IP pools, typically ranging from **500K to 200M+ IPs**.

![Example](https://media.discordapp.net/attachments/1366716403683426334/1431298769739190353/vnvGkIA.png?ex=6941765a\&is=694024da\&hm=7ff769efd537a8bb7d8336c084789591f8c9d68f20cea70847d640c70b1f1949&=\&format=webp\&quality=lossless)

---

## 3 - Setting Up a CAPTCHA Solver

A CAPTCHA solver is software that automatically solves CAPTCHAs for you. It is fast, reliable, and required for most tools.

Xtools supports **four different solvers**, allowing users to choose based on their budget and needs.

### Supported Solvers

* **ROSOLVE** — [https://rosolve.pro](https://rosolve.pro)
* **DEVIOUS** — [https://devioussolver.mysellauth.com](https://devioussolver.mysellauth.com)
* **CDS** — [https://t.me/cds_solve](https://t.me/cds_solve)
* **FUNBYPASS** — [https://funbypass.com](https://funbypass.com)

---

## 4 - Results & Output

Whenever a tool successfully performs an operation, it may generate a result. Only tools that require output will write data to the **`output` folder**, which is located in the same directory as the executable.

---

## Advanced / Custom Output

In Xtools, service owners and developers can control how data is output—whether for reselling, feeding results into custom tools, or other use cases.

The **Advanced Result** system (also called **Custom Output**) provides additional information such as:

* `user_id`
* Old and new passwords
* Old and new cookies
* Other relevant values depending on the tool

This allows for much more detailed and flexible data handling.

---

## Supported Tools & Output Formats

The following list explains what data each tool can output:

```
AccountChecker -- Added formatter (Success -> username, password, password_new, cookie | Fail -> username, password_new (original password))
AssetBooster -- Added formatter (Success -> username, user_id, password, cookie, asset_id)
AutoMedia -- No output
ClotchStealer -- No output
CookieChecker -- Added formatter (Success -> username, user_id, password, cookie | Invalid -> username, password, cookie)
CookieKiller -- SCRAPED
CookieRefresher -- Added formatter (Success -> username, password, cookie)
DeepDiagnose -- No output
Deschanger -- No output
Drainer -- Added formatter (Success -> username, user_id, password, cookie, total_drained)
EmailVerifier -- Added formatter (Success -> username, user_id, password, email, email_password, cookie)
GamepassGenerator -- Added formatter (Success -> username, user_id, password, gamepass_id, gamepass_link, cookie)
Generator -- Added formatter (Success -> username, password, cookie)
GroupBotter -- No output
GroupLeaver -- No output
GroupSniper -- Added formatter (Success -> group_id, group_link)
Humanizer -- Added formatter (Success -> username, user_id, password, cookie)
MassDisplayChanger -- No output
MassFav -- No output
MassFollower -- No output
MassFriender -- No output
MassPrivateServer -- Added formatter (Success -> username, user_id, password, private_server_link, cookie)
MassReporter -- No output
ModelVoter -- No output
PassChanger -- Added formatter (Success -> username, password, password_new, cookie, cookie_new, user_id)
PhoneVerifier -- Added formatter (Success -> username, number, ISO, user_id, cookie, password)
PlaceMassFav -- No output
RbxlMass -- No output
RbxmMass -- No output
SingleBuyer -- No output
Sniper -- Added formatter (Generated -> username, password, cookie | Sniped -> username)
WarningBypass -- No output
```

---
# Xtools UI – FAQ

This FAQ answers the most common questions new users ask when getting started with **Xtools UI**.

---

### 1. What proxy type should I use?

**Residential proxies** are the best and most reliable option. They offer higher success rates and lower detection compared to other proxy types.

---

### 2. How many CAPTCHA solver credits do I need?

It **totally depends on your tasks**. Some tools are designed to avoid CAPTCHAs when using **aged cookies** that are not heavily abused, which can significantly reduce solver usage.

---

### 3. Why do my cookies stop working after changing regions?

Roblox cookies are **region-locked**. If you use a proxy from the wrong region, the cookies have a very high chance of becoming invalid.

---

### 4. Which tools generate output files?

Check the **Advanced Output Formats** section. Any tool marked as **“No output”** will not generate result files.

---

### 5. Where can I see logs or errors?

All logs, errors, and status messages are displayed **directly in the console**.

---

### 6. Where are output formats configured?

Output formats are **preset by default** and can be found in:

```
config/OutputFormats
```

---

### 7. Can I use multiple CAPTCHA solvers at the same time?

No. **Only one solver can be used at a time**.

---

### 8. What should I do if I encounter an unknown issue?

If you face an issue you have never seen before, feel free to **DM the developers or the owner** for support.

---

If you’re still unsure about something, don’t hesitate to ask—this FAQ will continue to grow as new questions come up.

