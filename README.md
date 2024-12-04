Para ejecutar el proyecto:
```bash
python -m venv scrapyenv
source scrapyenv/Scripts/activate
python.exe -m pip install --upgrade pip
pip install -r requirements.txt 
scrapy startproject bookscrape
```
Fase de desarrollo-instalaciones:
Dentro de bookscrape ejecutar los suientes comandos:
```bash
cd bookscrape/bookscrape/spiders/ ejecutar -> scrapy genspider bookspyder books.toscrape.com
dentro de spider -> pip install ipython

```
En scrapy.sfg colocar:
```bash
[settings]
shell = ipython
```bash
dentro de spider -> scrapy shell
```
El entorno debe estar activo

abrimos la url con:
se debe cambiar ROBOTSTXT_OBEY = False en settings.py
```bash
fetch('https://books.toscrape.com/')
```
si colocas response debe salir <200 https://books.toscrape.com/>

books = response.css('article.product_pod')
book = books[0]
book.css('h3 a::text').get()

