Official Reddcoin Electrum Client - reference implementation
------------------------------------------------------------
* Licence: GNU GPL v3
* Author: Thomas Voegtlin
* Author: Larry Ren (laudney) forked for Reddcoin
* Language: Python
* Homepage: http://reddwallet.org

Getting Started
------------------
To install the wallet and all its dependencies, just do:

    sudo python setup.py install

Then you can run it from any directory:

    electrum

Or you can run it from the source code directory:

    ./electrum

How to Create Official Packages
------------------------------------
python mki18n.py
pyrcc4 icons.qrc -o gui/qt/icons_rc.py
python setup.py sdist --format=zip,gztar

On Mac OS X:

    # On port based installs
    sudo python setup-release.py py2app

    # On brew installs
    ARCHFLAGS="-arch i386 -arch x86_64" sudo python setup-release.py py2app --includes sip
    sudo hdiutil create -fs HFS+ -volname "Reddcoin Electrum" -srcfolder dist/Electrum.app dist/electrum-VERSION-macosx.dmg