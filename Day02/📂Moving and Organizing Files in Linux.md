
## 🚀 Moving a File

Move `styles.css` into the `css` directory:

```bash
mkdir css
mv styles.css css/
ls css
```

## ✏️ Renaming a File

Rename `index.html` to `home.html`:

```bash
mv index.html home.html
ls
```

## 📂 Moving Multiple Files

### 1️⃣ Creating a Directory

```bash
mkdir scripts
```

### 2️⃣ Moving JavaScript Files

```bash
mv *.js scripts/
ls scripts
```

## 🔒 Using `-i` for Safe Moves

### 📝 Creating a Test File

```bash
echo "Test content" > test.txt
```

### 🔍 Checking and Creating `home.html`

```bash
ls home.html || echo "Home page" > home.html
```

### ⚠️ Moving with Overwrite Prompt

```bash
mv -i test.txt home.html
```

## 🔧 Additional `mv` Options

|Option|Description|
|---|---|
|`-f`|Force move without prompt|
|`-n`|Do not overwrite existing files|
|`-v`|Verbose mode, explaining actions|

🚨 **Be cautious while moving files to avoid accidental overwrites!** 🚨