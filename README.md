# vorlagen
## Arbeitsblätter generieren
Docker muss installiert sein und laufen.
### Mit Inhaltsverzeichnis

```
docker run --rm \
    -v `pwd`:/data \
    -w /data \
    rstropek/pandoc-latex \
    -f markdown \
    --template https://raw.githubusercontent.com/gbssg/vorlagen/main/gbs.latex \
    -t latex \
-N \
    -o mydoc.pdf \
--toc \
-V lang=de \
    mydoc.md
```
    
### Ohne Inhaltsverzeichnis

```
docker run --rm \
    -v `pwd`:/data \
    -w /data \
    rstropek/pandoc-latex \
    -f markdown \
    --template https://raw.githubusercontent.com/gbssg/vorlagen/main/gbs.latex \
    -t latex \
-N \
    -o mydoc.pdf \
-V lang=de \
    mydoc.md
 ```
