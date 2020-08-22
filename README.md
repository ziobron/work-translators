# subtitles-translator

There are two python scripts:
* [subtitles_compressor.py](subtitles_compressor.py)
* [subtitles_translator.py](subtitles_translator.py)

---

## [`subtitles_compressor.py`](subtitles_compressor.py)

Since sentences are divided into fragments, first script connects them together and separates sentences from each other.

So for example from this .sbv subtitle:

```
0:00:10.068,0:00:12.637
Przejdźmy sobie do tych
kontenerów sekwencyjnych.

0:00:12.937,0:00:16.247
Wektor - to jest też taka tablica, tylko
mówimy, że ona jest już dynamiczna,

0:00:16.272,0:00:17.715
ponieważ może się rozszerzać.
```

You will get this output in other new file:

```
Przejdźmy sobie do tych kontenerów sekwencyjnych. 

Wektor - to jest też taka tablica, tylko mówimy, że ona jest już dynamiczna, ponieważ może się rozszerzać. 
```

Now you can make some corrections as well since program treats any dot '.' as the end of sentence (which isn't always the case).

---

## [`subtitles_translator.py`](subtitles_translator.py)

The only thing left is to translate sentences. After using file generated above, you will get this output:

```
Przejdźmy sobie do tych kontenerów sekwencyjnych. 
Let's move on to these sequence containers.

Wektor - to jest też taka tablica, tylko mówimy, że ona jest już dynamiczna, ponieważ może się rozszerzać. 
Vector - this is also an array, but we say that it is dynamic because it can expand.
```

Next to original sentence you have the translated version, so you can correct it.
After that you can copy/paste fragments of translated sentences directly into subtitles :)