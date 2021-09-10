# OpenWebText
Quickly and easily download the [OpenWebText Corpus](https://skylion007.github.io/OpenWebTextCorpus/).

## Extraction

```bash
# 1. Reassemble the split archive
cat openwebtext/openwebtext* > openwebtext.tar.xz

# 2. Extract to get individual .xz archives
tar -xf openwebtext.tar.xz

# 3. Extract each archive to get .txt files
mkdir -p extracted
for f in openwebtext/urlsf*.xz; do xzcat "$f" | tar -xf - -C extracted; done

# 4. Cleanup (optional)
rm openwebtext.tar.xz openwebtext/urlsf*.xz
```
