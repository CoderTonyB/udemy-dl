[![GitHub release](https://img.shields.io/badge/release-v0.5-brightgreen.svg?style=flat-square)](https://github.com/r0oth3x49/udemy-dl/releases/tag/v0.5)
[![GitHub stars](https://img.shields.io/github/stars/r0oth3x49/udemy-dl.svg?style=flat-square)](https://github.com/r0oth3x49/udemy-dl/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/r0oth3x49/udemy-dl.svg?style=flat-square)](https://github.com/r0oth3x49/udemy-dl/network)
[![GitHub issues](https://img.shields.io/github/issues/r0oth3x49/udemy-dl.svg?style=flat-square)](https://github.com/r0oth3x49/udemy-dl/issues)
[![GitHub license](https://img.shields.io/github/license/r0oth3x49/udemy-dl.svg?style=flat-square)](https://github.com/r0oth3x49/udemy-dl/blob/master/LICENSE)

update by tony b

# udemy-dl

**A cross-platform python based utility to download courses from udemy for personal offline use.**

[![udemy-dl-0-5.png](https://s26.postimg.cc/67x3wfak9/udemy-dl-0-5.png)](https://postimg.cc/image/s73ijmred/)

## **_Features_**

* Resume capability for a course video.
* Supports organization and individual udemy users both.
* Save course direct download links to a text file (option: `--save`).
* Cache credentials to a file and use it later for login purpose (option: `--cache`).
* List down course contents and video resolution, suggest the best resolution (option: `--info`).
* Download/skip all available subtitles for a video (options: `--skip-sub, --skip-sub`).
* Download spacific chapter in a course (option: `-c / --chapter`).
* Download specific lecture in a chapter (option: `-l / --lecture`).
* Download chapter(s) by providing range in a course (option: `--chapter-start, --chapter-end`).
* Download lecture(s) by providing range in a chapter (option: `--lecture-start, --lecture-end`).
* Download lecture(s) requested resolution (option: `-q / --quality`).
* Download course to user requested path (option: `-o / --output`).
* Authentication using cookies (option: `-k / --cookies`).
* Download/save lecture names (option: `--names`).
* Download lectures containing unsafe _unicode_ characters in title/name (option: `--unsafe`).

## **_Issue Reporting Guideline_**

To maintain an effective bugfix workflow and make sure issues will be solved, I ask reporters to follow some simple guidelines.

Before creating an issue, please do the following:

1.  **Use the GitHub issue search** &mdash; check if the issue has already been reported.
2.  **Check if the issue has been fixed** &mdash; try to reproduce it using the latest `master` in the repository.
3.  Make sure, that information you are about to report is related to this repository
    and not the one available **_Python's repository_**, Because this repository cannot be downloaded via pip.

A good bug report shouldn't leave others needing to chase you up for more
information. Please try to be as detailed as possible in your report. What is
your environment? What was the course url? What steps will reproduce the issue? What OS
experience the problem? All these details will help to fix any potential bugs as soon as possible.

### **_Example:_**

> Short and descriptive example bug report title
>
> A summary of the issue and the OS environment in which it occurs. If
> suitable, include the steps required to reproduce the bug.
>
> 1.  This is the first step
> 2.  This is the second step
> 3.  Further steps, etc.
>
> `<url>` - a udemy course link to reproduce the error.
>
> Any other information you want to share that is relevant to the issue being reported.

## **_Requirements_**

* Python (2 or 3)
* Python `pip`
* Python module `requests`
* Python module `colorama`
* Python module `unidecode`
* Python module `six`
* Python module `requests[security]` or `pyOpenSSL`

## **_Module Installation_**

    pip install -r requirements.txt

## **_Tested on_**

* Windows 7/8/8.1/10
* Kali linux (2017.2)
* Ubuntu-LTS (64-bit) (tested with super user)
* Mac OSX 10.9.5 (tested with super user)

## **_Download udemy-dl_**

You can download the latest version of udemy-dl by cloning the GitHub repository.

    git clone https://github.com/r0oth3x49/udemy-dl.git

## **_Usage_**

**_Download a course_**

    python udemy-dl.py COURSE_URL

**_Download course with specific resolution_**

    python udemy-dl.py COURSE_URL -q 720

**_Download course to a specific location_**

    python udemy-dl.py COURSE_URL -o "/path/to/directory/"

**_Download course with specific resolution to a specific location_**

    python udemy-dl.py COURSE_URL -q 720 -o "/path/to/directory/"

**_Download specific chapter from a course_**

    python udemy-dl.py COURSE_URL -c NUMBER

**_Download specific lecture from a chapter_**

    python udemy-dl.py COURSE_URL -c NUMBER -l NUMBER

**_Download lecture(s) range from a specific chapter_**

    python udemy-dl.py COURSE_URL -c NUMBER --lecture-start NUMBER --lecture-end NUMBER

**_Download chapter(s) range from a course_**

    python udemy-dl.py COURSE_URL --chapter-start NUMBER --chapter-end NUMBER

**_Download specific lecture from chapter(s) range_**

    python udemy-dl.py COURSE_URL --chapter-start NUMBER --chapter-end NUMBER --lecture NUMBER

**_Download lecture(s) range from chapter(s) range_**

    python udemy-dl.py COURSE_URL --chapter-start NUMBER --chapter-end NUMBER --lecture-start NUMBER --lecture-end NUMBER

**_List down specific chapter from a course_**

    python udemy-dl.py COURSE_URL -c NUMBER --info

**_List down specific lecture from a chapter_**

    python udemy-dl.py COURSE_URL -c NUMBER -l NUMBER --info

## **Advanced Usage**

<pre><code>
Author: Nasir khan (<a href="http://r0oth3x49.herokuapp.com/">r0ot h3x49</a>)

usage: udemy-dl.py [-h] [-v] [-u] [-p] [-k] [-o] [-q] [-c] [-l]
                   [--chapter-start] [--chapter-end] [--lecture-start]
                   [--lecture-end] [--save] [--info] [--cache] [--names]
                   [--unsafe] [--sub-only] [--skip-sub]
                   course

A cross-platform python based utility to download courses from udemy for
personal offline use.

positional arguments:
  course            Udemy course.

General:
  -h, --help        Shows the help.
  -v, --version     Shows the version.

Authentication:
  -u , --username   Username in udemy.
  -p , --password   Password of your account.
  -k , --cookies    Cookies to authenticate with.

Advance:
  -o , --output     Download to specific directory.
  -q , --quality    Download specific video quality.
  -c , --chapter    Download specific chapter from course.
  -l , --lecture    Download specific lecture from chapter(s).
  --chapter-start   Download from specific position within course.
  --chapter-end     Download till specific position within course.
  --lecture-start   Download from specific position within chapter(s).
  --lecture-end     Download till specific position within chapter(s).

Others:
  --save            Do not download but save links to a file.
  --info            List all lectures with available resolution.
  --cache           Cache your credentials to use it later.
  --names           Do not download but save lecture names to file.
  --unsafe          Download all course with unsafe names.
  --sub-only        Download captions/subtitle only.
  --skip-sub        Download course but skip captions/subtitle.

Example:
  python udemy-dl.py  COURSE_URL
  python udemy-dl.py  COURSE_URL -k cookies.txt
  python udemy-dl.py -u user@domain.com -p p4ssw0rd COURSE_URL
</code></pre>
