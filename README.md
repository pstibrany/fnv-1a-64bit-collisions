# Some FNV-1a (64-bit) collisions

* `8yn0iYCKYHlIj4-BwPqk` and `GReLUrM4wMqfg9yzV3KQ` hash to 0x4EAC0C95540867E4.
* `gMPflVXtwGDXbIhP73TX` and `LtHf1prlU1bCeYZEdqWf` hash to 0x8FCF3BE2DE898214.
* `pFuM83THhM-Qw8FI5FKo` and `.jPx7rOtTDteKAwvfOEo` hash to 0xF8893E25250C0EAA.
* `7mohtcOFVz` and `c1E51sSEyx` hash to 0x184ADE9A961953A2
* `6a5x-VbtXk` and `f_2k7GG-4v` hash to 0x703C4DD295D7AA15

Collisions specific for [Prometheus](https://github.com/prometheus/common/blob/b5fe7d854c42dc7842e48d1ca58f60feae09d77b/model/signature.go#L56)/[Cortex](https://github.com/cortexproject/cortex/blob/241d457f999f320f7f337f69722128078837ee48/pkg/ingester/client/compat.go#L249)/Loki `Fingerprint` function, which uses repeated string `<label name>\xff<label value>\xff` for each label, where labels are sorted by name, and label names match regex `[a-zA-Z_][a-zA-Z0-9_]*`.

* `_\xffypfajYg2lsv` and `_\xffKiqbryhzUpn` both hash to 0xC525E0FD0A130EF0.
* `A\xffK6sjsNNczPl` and `A\xffcswpLMIZpwt` have same FNV-1a hash 0xF691F0E8B57A7DF.

