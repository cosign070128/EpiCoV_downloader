# GISAID EpiCoV Downloader

This is a GISAID downloader to retrieve all EpiCoV sequences and the table. The script utilies selenium to acess GISAID website through a Firefox webdriver.

## Requirements
You may need to install firefox and geckodriver to run the downloader other than selenium. Below is an example using conda:

```bash
$ conda install -c conda-forge selenium geckodriver firefox
```

## Usage
```bash
usage: gisaid_EpiCoV_downloader.py [-h] -u [STR] -p [STR] [-o [STR]]
                                   [-cs [YYYY-MM-DD]] [-ce [YYYY-MM-DD]]
                                   [-ss [YYYY-MM-DD]] [-se [YYYY-MM-DD]] [-cg]
                                   [-hc] [-t [INT]] [-r [INT]] [-i [INT]] [-m]
                                   [--headless]

Download all EpiCoV sequcnes from GISAID

optional arguments:
  -h, --help            show this help message and exit
  -u [STR], --username [STR]
                        GISAID username
  -p [STR], --password [STR]
                        GISAID password
  -o [STR], --outdir [STR]
                        Output directory
  -cs [YYYY-MM-DD], --colstart [YYYY-MM-DD]
                        collection starts date
  -ce [YYYY-MM-DD], --colend [YYYY-MM-DD]
                        collection ends date
  -ss [YYYY-MM-DD], --substart [YYYY-MM-DD]
                        submitssion starts date
  -se [YYYY-MM-DD], --subend [YYYY-MM-DD]
                        submitssion ends date
  -cg, --complete       complete genome only
  -hc, --highcoverage   high coverage only
  -t [INT], --timeout [INT]
                        set action timeout seconds. Default is 90 secs.
  -r [INT], --retry [INT]
                        retry how many times when the action fails. Default is
                        5 times.
  -i [INT], --interval [INT]
                        time interval between retries in second(s). Default is
                        3 seconds.
  -m, --meta            download metadata
  --headless            turn on headless mode
```
