# Calibre Weblibrary Downloader

Python-script to download books from a publicly accessible library. A great way to find new ones is by using [Shodan](https://www.shodan.io/search?query=%22server%3A+calibre%22). 

Please note that I am in no way encouraging neither copyright infringement nor unauthorized access, as I assume anyone sharing their calibre library are doing so with the full knowledge that all their books are accessible online, and therefore only shares works that are in the public domain.

### Prerequisites

* Python v3

* BeautifulSoup 
```
python3 -m pip install beautifulsoup4
```

* fake-useragent
```
python3 -m pip install fake-useragent
```
* Requests
```
python3 -m pip install requests

```


## Usage

1. Edit [libraryStorage](https://github.com/kopach/CalibreWeblibraryDownloader/blob/master/CalibreWeblibraryDownloader.py#L483) variable. Pass path to the directory, where books should be saved to.

2. (Optionally) Edit list of file formats you want to be downloaded [wantedFormats](https://github.com/kopach/CalibreWeblibraryDownloader/blob/master/CalibreWeblibraryDownloader.py#L481)

3. Just run the script and pass either an adress in the format of ip:port, or a file with lots of adresses (one per line).


## Note

You'll need to configure a path of where to save the downloaded books, the libraryStorage-variable. Also, I myself don't care for pdf's, so I'm ignoring them, but if you want those you'll have to adjust the code a bit.


## To-Do

* Add argparse to get a better grip of parameters. (Like: -f "EPUB, MOBI" for formats.)
* Remove reliance of fake-useragent by hardcoding a list of useragents. Don't know if this is better or not, might skip it.
* (Maybe) Figure out a way to redo the whole rule-handling, to be able to make more complex rules.
* (Maybe) Create a version which scrapes the pages using selenium, so as not to be limited to the mobile page and thereby getting a better metadata-selection, like Language, Tags, Series etc.


## Authors

* **Knarkoffer** - *Author* - [Knarkoffer](https://github.com/Knarkoffer)


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Kovid Goyal for creating the excellent application calibre
* Thanks to the creators of BeautifulSoup for their excellent way of processing HTML-code
* Other creators of libraries I've used
