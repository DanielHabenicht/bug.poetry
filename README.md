# bug.poetry

```
pip install poetry
poetry new example
cd example
mkdir folder
cd folder
for i in {1..70000}; do
  mkdir s"$i"
  touch s"$i"/file1.file
  touch s"$i"/file2.file
  touch s"$i"/file3.file
done
```

Takes no effect:

```toml
[tool.poetry]
exclude = ["folder"]
```
