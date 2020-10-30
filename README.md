# Symbol2Vec
Symbol2Vec embeddings for functions from C binaries in Debian.

The repository contains 3 fastText models. `model.old` contains a model based on an older analysis of
binaries. This analysis was run on 17,000 binaries but may have missed jump targets. Models under `model.new` were generated from 
more complete static analysis but only uses 11,000 binaries.


Models can be loaded with fastText [1] e.g.

```
./fastText analogies ./model.bin
> sha1_init_ctx md5_init_ctx md5_update
```

[1] https://github.com/facebookresearch/fastText
