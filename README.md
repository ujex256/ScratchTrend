<div align="center"><img src="https://user-images.githubusercontent.com/105550500/197376654-a36e55d0-35ac-42c8-aed5-23e9a48c04fd.jpg" /></div>

# ScratchTrend
[![PyPI](https://img.shields.io/badge/PyPI-dummy?style=for-the-badge&logo=pypi&labelColor=gray&color=red)](https://pypi.org/project/scratchtrend/)
[![GitHub](https://img.shields.io/badge/GitHub-dummy?style=for-the-badge&logo=github&labelColor=gray&color=blue)](https://github.com/henji243/ScratchTrend)

[![License](https://img.shields.io/github/license/henji243/ScratchTrend)](https://github.com/henji243/ScratchTrend)
[![Downloads](https://img.shields.io/pypi/dd/scratchtrend?color=%2383ccd2&label=PyPI%20Downloads&logo=PyPI&logoColor=%2383ccd2)](https://pypi.org/project/scratchtrend)

ScratchTrend retrieves popular works from https://scratch.mit.edu/explore.
<br />
<span style="color:red;">**(This library is not affiliated with the Scratch Foundation.)**</span><br/>
(日本語版は[ここ](https://github.com/henji243/ScratchTrend/blob/main/README_ja.md)からどうぞ。)
<br /><br />
# Usage
## Install
Terminal
```sh
$ pip install scratchtrend
```
Import
```python
import scratchtrend as sct
from scratchtrend.select import Lang, Sort
```
**Required Modules or Application**
- **Chrome Browser**
- Selenium
- BeautifulSoup
- chromedriver_binary  (It will automatically pass through the chromedriver Path)
<br /><br />

## Setup
```python
# example
data = sct.connect(Lang.JAPANESE, Sort.POPULAR)
```
The list of languages that can be specified is in Languages.md.
Specify language and sorting by ```connect()``` method.<br />
Sort by:
| Choose | Sort |
| ------- | ------- |
| Sort.TRENDING | Trending |
| Sort.POPULAR | Popular |
| Sort.RECENT | Recent |
<br />

## Method
(Still in the process of development, so there are few.)
```python
data.get_by_page()  # Get by specifying a page
data.get_by_rank()  # Get by specifying a rank
```
The ```get_by_page()``` method gets the works of the page from the start argument to the end argument.Be sure to use start&lt;end.<br />
The ```get_by_rank()``` method retrieves the works of rank from the start argument to the end argument.Be sure to use start&lt;end.
##### The term "rank" is a bit misleading. If you have a better way to say it, please contact Issues.
<br />

**Return value**
```python
# Formatted for ease of viewing.
[
    {
        'title': 'project title',
        'id': "project id"
    },
    {
        'title': 'title',
        'id': "ID"
    }
]
```
Thus, it is returned in the dictionary in the list.
<br /><br />
# DEMO
<a href="https://youtu.be/P-7ia4hHtjY" target="_blank"><img src="https://user-images.githubusercontent.com/105550500/198833200-901bc950-6799-4ec0-852a-8a1af70ee87f.png" alt="DemoVideo" /></a>


# Other
## License
ScratchTrend is MIT licensed.
## Credits
- Logo generated by <a href="https://www.designevo.com/" title="Free Online Logo Maker">DesignEvo free logo designer</a>
- [**Selenium**](https://github.com/SeleniumHQ/selenium)
- [**BeautifulSoup**](https://www.crummy.com/software/BeautifulSoup/)
- Translation was done using [**DeepL.**](https://www.deepl.com/translator)

## Contact
If you find a bug, please contact [Issue](https://github.com/henji243/ScratchTrend/issues) or [Scratch](https://scratch.mit.edu/projects/753404201/).
