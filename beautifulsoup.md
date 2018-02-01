### BeautifulSoup
```
pip3 install bs4
from bs4 import BeautifulSoup
... //get html
bsObj = BeautifulSoup(html)

bsObj.findAll(tgbName,tagAttributes)
// tagName 'h1' or {'h1','h2','h3'}
// tagAttributes => {attributeName:attributeValue}
```
处理子标签：find findAll

处理兄弟标签：next_siblings previous_siblings

处理父标签：parent
