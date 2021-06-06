#### usage

```
nohup python3 run.py &
```

#### structure 

``` 
.
├── README.md
├── run.py
├── data_fetch.py
├── process.py
├── Gaia_info.csv
├── Gaia_info_old.csv
├── log
│   └── log_20210529
└── raw
    ├── Gaia21ccb
    │   ├── light curve,HR diagram, etc
    ├── Gaia21ccw
    ├── ...
```

#### config

- filter :
   - Whitelist = ['lens' , 'brighter' , 'ULENS' , 'rise']
   - Blacklist = ['SN' , 'QSO' , 'galaxy' , 'Blazer' , 'BL Lac']
   - selected = Whitelist AND (NOT Blacklist)

#### explanation

- Can :
   - -1         NOT checked
   - 0          checked but NOT chosen as ulens candidate
   - 0.5        checked but NOT sure 
   - 1          checked and CHOSEN as  ulens candidate

- status :
   - 1          being monitored
   - 0          NOT being monitored
   - default    0
