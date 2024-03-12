---
id: jre1lif6kmflrldqh6bf2lr
title: Install from Source
desc: ''
updated: 1709872467761
created: 1709703758475
---

#### 1. Install rust

```bash
curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

then afte installation is successful:

```bash
source ~/.cargo/env 
```

```bash
rustc --version
```

#### 2. Build rust

```bash
git clone https://github.com/helix-editor/helix.git
```

```bash
cd helix
```

```bash
cargo install --path helix-term --locked
```

> No problems in installation even in my *Oracle linux 8

### Runtime Files
For me adding the following to `.bashrc` doesn't work
```bash
HELIX_RUNTIME=~/Source-Code/helix/runtime

```

*Solution:* Instead of the above. Go to the `~/Source-Code/helix`(helix source code) diectory and run :
```bash
ln -Ts $PWD/runtime ~/.config/helix/runtime
```

