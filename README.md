**EasyCoin**
Basically just a fork of CryptoNote. Not much changed, even default ports. Only change that matters is setting Target Diff time to 60 seconds instead of 120 seconds. Also fixed the in CMakeLists in src so it doesn't throw ConnectivityTool error while compiling.



**1. Clone wallet sources**

```
git clone https://github.com/cryptonotefoundation/cryptonotewallet.git
```

**2. Modify `CryptoNoteWallet.cmake`**
 
```
set(CN_PROJECT_NAME "furiouscoin")
set(CN_CURRENCY_DISPLAY_NAME "FuriousCoin")
set(CN_CURRENCY_TICKER "XFC")
```

**3. Set symbolic link to coin sources at the same level as `src`. For example:**

```
ln -s ../cryptonote cryptonote
```

Alternative way is to create git submodule:

```
git submodule add https://github.com/cryptonotefoundation/cryptonote.git cryptonote
```

Replace URL with git remote repository of your coin.

**4. Build**

```
mkdir build && cd build && cmake .. && make
```
