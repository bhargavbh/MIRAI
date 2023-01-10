# Recommended Configs for Polakdot repos

Building with `cargo mirai` works on Polkadot, Smoldot, and ink repos. 
To get an idea of the kind of warnings geenrated by MIRAI, recommend using the `diag=paranoid` mode and `MIRAI_LOGS` flag set to "warn" or "info". These can be set as environment varibles (`[env]`) in the .cargo/config.toml configuration file of the crate where you run cargo mirai. 

```
[env]

MIRAI_FLAG = "--diag=paranoid --print_function_names"
MIRAI_LOGS = "warn"
```


If the tool prints time-out warnings while analysisng function, you can increase the time-out duration by setting the `MIRAI_FLAGS` variable to `--body_analysis_timeout <in secs>`. The default is set to `20s` per entry point. 

More information on the configuration options can be found [here](https://github.com/bhargavbh/MIRAI/blob/main/README.md)
