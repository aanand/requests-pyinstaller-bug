Run `make` inside this directory to test the requests/pyinstaller bug:

    $ make
    script/build-linux
    >> Building Docker image
    >> Running bin/test
    Importing requests
    Imported requests 2.6.0
    >> Building dist/test
    >> Running dist/test
    Importing requests
    Traceback (most recent call last):
      File "<string>", line 3, in <module>
      File "/usr/local/lib/python2.7/dist-packages/PyInstaller/loader/pyi_importers.py", line 276, in load_module
        exec(bytecode, module.__dict__)
      File "/code/build/test/out00-PYZ.pyz/requests", line 58, in <module>

      File "/usr/local/lib/python2.7/dist-packages/PyInstaller/loader/pyi_importers.py", line 276, in load_module
        exec(bytecode, module.__dict__)
      File "/code/build/test/out00-PYZ.pyz/requests.utils", line 26, in <module>
      File "/usr/local/lib/python2.7/dist-packages/PyInstaller/loader/pyi_importers.py", line 276, in load_module
        exec(bytecode, module.__dict__)
      File "/code/build/test/out00-PYZ.pyz/requests.compat", line 7, in <module>
      File "/usr/local/lib/python2.7/dist-packages/PyInstaller/loader/pyi_importers.py", line 276, in load_module
        exec(bytecode, module.__dict__)
      File "/code/build/test/out00-PYZ.pyz/requests.packages.chardet", line 19, in <module>
      File "/code/build/test/out00-PYZ.pyz/requests.packages", line 95, in load_module
    ImportError: No module named 'requests.packages.chardet.sys'
    make: *** [default] Error 255