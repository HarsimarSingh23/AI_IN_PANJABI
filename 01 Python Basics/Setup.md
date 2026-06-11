macOS ਉੱਤੇ Python install ਕਰਨਾ -

1. ਆਪਣੇ Mac ਉੱਤੇ Terminal application ਖੋਲ੍ਹੋ।
2. ਇਹ ਤੁਹਾਨੂੰ Applications folder ਦੇ ਅੰਦਰ Utilities folder ਵਿੱਚ ਮਿਲ ਜਾਵੇਗੀ, ਜਾਂ ਤੁਸੀਂ Spotlight ਨਾਲ search ਕਰ ਸਕਦੇ ਹੋ।
3. ਜਦੋਂ Terminal ਖੁੱਲ੍ਹ ਜਾਵੇ, ਤਾਂ ਇਹ check ਕਰਨ ਲਈ ਕਿ Python ਪਹਿਲਾਂ ਤੋਂ install ਹੈ ਜਾਂ ਨਹੀਂ, ਹੇਠਾਂ ਦਿੱਤੀ command type ਕਰੋ ਅਤੇ Enter ਦਬਾਓ:

```bash
python3 --version
```

4. ਜੇ Python install ਹੈ, ਤਾਂ ਤੁਹਾਨੂੰ version number ਦਿਖਾਈ ਦੇਵੇਗਾ। ਜੇ install ਨਹੀਂ ਹੈ, ਤਾਂ ਤੁਹਾਨੂੰ error message ਮਿਲੇਗਾ।
5. ਜੇ Python install ਨਹੀਂ ਹੈ, ਤਾਂ ਤੁਸੀਂ ਇਸਨੂੰ Homebrew ਰਾਹੀਂ install ਕਰ ਸਕਦੇ ਹੋ, ਜੋ macOS ਦਾ ਇੱਕ package manager ਹੈ। ਜੇ ਤੁਹਾਡੇ ਕੋਲ Homebrew install ਨਹੀਂ ਹੈ, ਤਾਂ Terminal ਵਿੱਚ ਇਹ command run ਕਰਕੇ install ਕਰ ਸਕਦੇ ਹੋ:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

6. Homebrew install ਹੋਣ ਤੋਂ ਬਾਅਦ, ਤੁਸੀਂ ਹੇਠਾਂ ਦਿੱਤੀ command run ਕਰਕੇ Python install ਕਰ ਸਕਦੇ ਹੋ:

```bash
brew install python
```

7. Installation ਪੂਰੀ ਹੋਣ ਤੋਂ ਬਾਅਦ, ਤੁਸੀਂ ਦੁਬਾਰਾ ਇਹ command run ਕਰਕੇ verify ਕਰ ਸਕਦੇ ਹੋ ਕਿ Python install ਹੋ ਗਿਆ ਹੈ:

```bash
python3 --version
```

8. ਹੁਣ ਤੁਹਾਨੂੰ ਉਸ Python ਦਾ version number ਦਿਖਾਈ ਦੇਵੇਗਾ ਜੋ ਤੁਸੀਂ ਹੁਣੇ install ਕੀਤਾ ਹੈ। ਤੁਸੀਂ ਹੇਠਾਂ ਦਿੱਤੀ command type ਕਰਕੇ Python interpreter ਵੀ start ਕਰ ਸਕਦੇ ਹੋ:

```bash
python3
```

9. ਇਸ ਨਾਲ Python interactive shell ਖੁੱਲ੍ਹ ਜਾਵੇਗਾ, ਜਿੱਥੇ ਤੁਸੀਂ Python code ਲਿਖਣਾ ਅਤੇ execute ਕਰਨਾ ਸ਼ੁਰੂ ਕਰ ਸਕਦੇ ਹੋ। Interactive shell ਤੋਂ ਬਾਹਰ ਆਉਣ ਲਈ, `exit()` type ਕਰੋ ਅਤੇ Enter ਦਬਾਓ।
10. ਵਧਾਈਆਂ! ਤੁਸੀਂ macOS ਉੱਤੇ Python ਸਫਲਤਾਪੂਰਵਕ install ਕਰ ਲਿਆ ਹੈ। ਹੁਣ ਤੁਸੀਂ Python ਸਿੱਖਣਾ ਅਤੇ ਇਸ ਵਿੱਚ coding ਕਰਨਾ ਸ਼ੁਰੂ ਕਰ ਸਕਦੇ ਹੋ!
11. ਹਮੇਸ਼ਾ Python ਦਾ ਨਵਾਂ version download ਕਰੋ ਤਾਂ ਜੋ ਤੁਹਾਨੂੰ ਨਵੇਂ features ਅਤੇ security updates ਮਿਲ ਸਕਣ। ਤੁਸੀਂ Python ਦੀ official website ਤੋਂ updates check ਕਰ ਸਕਦੇ ਹੋ ਅਤੇ latest version download ਕਰ ਸਕਦੇ ਹੋ: https://www.python.org/downloads/
12. ਜੇ ਤੁਸੀਂ Python development ਲਈ ਕੋਈ Integrated Development Environment (IDE) ਵਰਤਣਾ ਪਸੰਦ ਕਰਦੇ ਹੋ, ਤਾਂ ਤੁਸੀਂ PyCharm, Visual Studio Code, ਜਾਂ Jupyter Notebook ਵਰਗੇ popular IDEs install ਕਰ ਸਕਦੇ ਹੋ। ਇਹ IDEs ਤੁਹਾਡੇ coding experience ਨੂੰ ਬਿਹਤਰ ਬਣਾਉਣ ਲਈ extra features ਅਤੇ tools ਦਿੰਦੇ ਹਨ।
13. ਆਪਣੀ Python installation ਨੂੰ up to date ਰੱਖੋ ਅਤੇ ਸਮੇਂ-ਸਮੇਂ ਉੱਤੇ updates check ਕਰਦੇ ਰਹੋ ਤਾਂ ਜੋ ਤੁਹਾਨੂੰ ਨਵੇਂ features ਅਤੇ security patches ਮਿਲਦੇ ਰਹਿਣ। ਤੁਸੀਂ ਆਪਣੀਆਂ programming capabilities ਵਧਾਉਣ ਲਈ ਹੋਰ Python libraries ਅਤੇ frameworks ਵੀ explore ਕਰ ਸਕਦੇ ਹੋ। Happy coding!



## ਸ਼ੁਰੂ ਕਰਨ ਅਤੇ ਬਹੁਤ ਆਸਾਨੀ ਨਾਲ ਸਿੱਖਣ ਲਈ ਇਸ ਵੈੱਬਸਾਈਟ 'ਤੇ ਜਾਓ -
## https://www.programiz.com/python-programming/online-compiler/