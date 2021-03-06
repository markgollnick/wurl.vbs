wurl.vbs
========

An HTTP file downloader (inspired by [curl][] and GNU [wget][]) written in
VBScript, and callable from Windows batch scripts. The name "wurl" is a mixture
of "wget" and "curl". Or, it could stand for "Windows URL". You decide...

[wget]: http://gnuwin32.sourceforge.net/packages/wget.htm
[curl]: http://curl.haxx.se/


Rationale
---------

Ever needed to do some automated downloading and post-installation steps
following the set-up of a fresh installation of Windows? Or, ever wished you
could download stuff from the comfort and convenience of a batch script
without having to first fetch/package additional executables and their
libraries? Yeah...

Hence wurl.vbs, which is runnable on out-of-the-box set-ups of Windows and
callable from simple batch scripts, thus supporting automated silent downloads.

Use it wisely!


Requirements
------------

* cscript.exe (CLI)
* wscript.exe (GUI; default for double-click of VBS file)

...Both of which come with Windows, so nothing is really required (aside from
Windows itself) for wurl.vbs to run. :-)


Usage
-----

CLI Execution:

    cscript wurl.vbs <url> [save_to_file] [[/Y]|[/NC]]

GUI Execution:

    wscript wurl.vbs <url> [save_to_file] [[/Y]|[/NC]]

* `/Y`: Suppresses prompting to confirm you want to overwrite an existing
  destination file.

* `/NC`: No clobber: skip downloads that would download to existing files
  (overwriting them).


License
-------

Boost Software License, Version 1.0: <http://www.boost.org/LICENSE_1_0.txt>


Acknowledgements
----------------

Because writing VBScript is hard, (mind-numbingly so,) I'd like to give a
grateful shout-out to these like-minded fellows:

* Vittorio Pavesi ([wget.vbs][1], Sep 2005)
* Chrissy LeMaire ([fileFetch.vbs][2], Jan 2007)
* James "HM2K" Wade ([wget.vbs][3], Dec 2009)
* Mahmoud Abu-Ghali ([wget.vbs][4], Apr 2011)
* Jean-Hervé Lescop and all the folks at [Adersoft][] for [VbsEdit][] (2001)

[1]: http://vittoriop77.altervista.org/vbscripts/wget.html
[2]: http://blog.netnerds.net/2007/01/vbscript-download-and-save-a-binary-file/
[3]: https://code.google.com/p/hm2k/source/browse/trunk/code/vbs/wget.vbs
[4]: http://abu-ghali.com/2012/04/11/wget-for-windows/
[Adersoft]: http://adersoft.com/
[VbsEdit]: http://vbsedit.com/
