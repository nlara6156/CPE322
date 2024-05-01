## Lab 10

### Run #1 of Hash Value

```
PS C:\Users\nadia\iot\lesson10> python3 hash_value.py
The hash for 1 is: 1
The hash for 1.0 is: 1
The hash for 3.14 is: 322818021289917443
The hash for Python is: -8618236071167298098
The hash for a tuple of vowels is: 9185075461943906823
The hash for an object of person is: -4111237402702381223
```

### Run #2 of Hash Value

```
PS C:\Users\nadia\iot\lesson10> python3 hash_value.py
The hash for 1 is: 1
The hash for 1.0 is: 1
The hash for 3.14 is: 322818021289917443
The hash for Python is: 7837300043454952309
The hash for a tuple of vowels is: -8255807982862756380
The hash for an object of person is: 3716378598450869949
```

### SHA-2 Secure Hash Algorithm

```
PS C:\Users\nadia\iot\lesson10> python3
Python 3.9.6 (default, Jul 25 2021, 21:17:24)
[GCC 10.2.0] on cygwin
Type "help", "copyright", "credits" or "license" for more information.
>>> import hashlib
>>> m = hashlib.sha256(b"hello,world")
>>> m.hexdigest()
'77df263f49123356d28a4a8715d25bf5b980beeeb503cab46ea61ac9f3320eda'
>>> m.digest_size
32
>>> m.block_size
64
```


### Tiniest Blockchain (Run of snakecoin.py)

```
PS C:\Users\nadia\iot\lesson10> python3 snakecoin.py
Block #1 has been added to the blockchain!
Hash: e38522352fb6f95bd36e2eaa0b1dd393514126846da7bb84d78bebf60cccfa26

Block #2 has been added to the blockchain!
Hash: e9ece3239510ebde9e299ae8c887e398e61dfccc74fd599c402effdc24bed5a2

Block #3 has been added to the blockchain!
Hash: 8515043eee8cf43a758a86918f4c2c52ca4a9e87b4a591d1ebe8a29f8fc08ead

Block #4 has been added to the blockchain!
Hash: 2cd16937d1031b042b5e4d98f6f0ed3e1c6cfd0574f06ae47c2c1f24b4549233

Block #5 has been added to the blockchain!
Hash: 898ca588ecc3eebc036ecd00585e028e8b72f1917cade64206213fb1bcb5f957

Block #6 has been added to the blockchain!
Hash: 6e2e2f760f55c7c4268c597862fcf093f97add013d13714443eb9c3e490fd22d

Block #7 has been added to the blockchain!
Hash: 1084dc3be1143890d8c227169183abfd4405dda36ef77e5f9179a2860516b093

Block #8 has been added to the blockchain!
Hash: 427ee13d576d4c42a9ae47dc6673bb5ba8821c182850dd040b68e441175b4f8f

Block #9 has been added to the blockchain!
Hash: 9f3194fabed759d0a9923e99c4e49f88e6ced39f5283df295c92c2412089372f

Block #10 has been added to the blockchain!
Hash: 6ea343e396be87bc641a97e87027ff513f59d6b2ed147e8966e658640b8c9b3c

Block #11 has been added to the blockchain!
Hash: d8bdae2583729c84cde406f3f1e844330ad0e026f746af5d7c63e10162d408c4

Block #12 has been added to the blockchain!
Hash: 581328b5f02f2efca371d42f57bf11c2dcade193c99c6f3bd30c45d4a516e918

Block #13 has been added to the blockchain!
Hash: cb24c2147a45e01d84b1a01043ed32d45ab964a9a5717fa133331a8b5cc11ebc

Block #14 has been added to the blockchain!
Hash: 49084effa25f31a85ae73f530aab96e75b78b492995aaa8c7ce6d4ae36c34414

Block #15 has been added to the blockchain!
Hash: 2cae77e4ee5860990bc889086952f0cfcdaed7cf46ef926f2bdf46ec237e15b6

Block #16 has been added to the blockchain!
Hash: 232289b02c561e42ab3ccf4ca9cd8d6e28b7b1751625a2520313040b50124739

Block #17 has been added to the blockchain!
Hash: 03d5421764133b1bf72a0dbc01d11313d771647a8f4da98fe5d1ed6b911bfdea

Block #18 has been added to the blockchain!
Hash: 5a2a85e928528e0b99fd5dafca42d98dd9624f8b3f2452d2400fe6ad6e577cc8

Block #19 has been added to the blockchain!
Hash: 82c6a90d55cf63ac023264c3bdca0f93dc22f02add9af37e724b0f0c4fc53b37

Block #20 has been added to the blockchain!
Hash: 2000d88e1207889562d273d28f5941f1a6000de9e67205b60647b21f2c507253
```

### Make Blockchain Bigger (Snakecoin-server-full-code.py)

![Fig1Lab10](images/Screenshot(273).png)

![Fig2Lab10](images/Screenshot(272).png)

### Blockchain App

![Fig3Lab10](images/Screenshot(274).png)

![Fig4Lab10](images/Screenshot(275).png)

![Fig5Lab10](images/Screenshot(276).png)

![Fig2Lab10](images/Screenshot(277).png)
