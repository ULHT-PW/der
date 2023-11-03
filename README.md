# Visualização de Diagrama Entidade Relação (DER)

instalação dos modulos:
```
pip install pygraphviz
pip install pydot
```


no ficheiro settings.py:

```Python
# settings.py
INSTALLED_APPS += ['django_extensions’]

GRAPH_MODELS = {
  'all_applications': True,
  'group_models': True,
}
```

para gerar uma imagem do DER:
```Python
python manage.py graph_models -a -o myapp_models.dot
dot -Tpng myapp_models.dot -o output.png
```
