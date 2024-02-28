---
id: w9ohh1flznuf22296abp97e
title: Plugins
desc: ''
updated: 1709104344746
created: 1709102311441
---


## Way - 1 (Install plugin directly)

Plugins are installed in `$HOME/.config/kak/autoload/`

Simply clone your plugin repo in this directory and `kakoune` will recursively search for `.kak` file and load the plugin

> But this will disable the default plugins

---

## 2. Using Plugin Manager

### 1. Install the plugin manager:

```bash
mkdir -p $HOME/.config/kak/autoload/bundle/
```

```bash
git clone https://github.com/jdugan6240/kak-bundle $HOME/.config/kak/autoload/bundle/kak-bundle
```


> Note: Problems with this method
> 1. You can't use the default plugins if you use the `autoload` directory
> 2. You'll have to manage this plugin manger on your own (ex: update)

**Better way:**

```bash
mkdir -p $HOME/.config/kak/bundle/
 ```

```bash
git clone https://github.com/jdugan6240/kak-bundle $HOME/.config/kak/bundle/kak-bundle
```

Then in your `kakrc` add the following lines to source `plugin manager`:

```kakrc
source "%val{config}/bundle/kak-bundle/rc/kak-bundle.kak"
bundle-noload kak-bundle https://github.com/jdugan6240/kak-bundle
```

- *Reference* : https://github.com/jdugan6240/kak-bundle

### 2. Install the plugins

**1. Register the plugins in `kakrc` :**

```kakrc
bundle kakboard https://github.com/lePerdu/kakboard %{
  # Configure here...
  hook global WinCreate .* %{ kakboard-enable }
}
```

**2. Run `bundle-install` command**