======================
Trace Collector Server
======================

A server for collecting tracing data from emscripten-compiled
applications including memory profiling information.

Note: This codes are cloned from original implementation by waywardmonkeys_.

.. _waywardmonkeys: https://github.com/waywardmonkeys/emscripten-trace-collector

Prerequisite
==================
Set up a Python virtual environment::

  virtualenv venv
  source venv/bin/activate

Make sure Python (< 3.10) is installed in your system or change the python version in your terminal by ``pyenv``. And activate the created virtual environment::

  source venv/bin/activate

Then install the dependent python packages by below commands::

  pip install setuptools==57.4.0 (if setuptools has been installed, uninstall it first)
  pip install -r requirements.txt
  pip install Flask-Cors

The reason why we install the specific version of ``setuptools``, it's that the ``Jinja2`` (2.7.3) only support the older version of ``setuptools``.

Running The Server
==================
Run the script::

  python ./run-server.py


Collect Data
==================
Make sure your client has configured the Emscripten trace tools in your source codes, you can check out the Emscripten document_ for more details.

.. _document: https://emscripten.org/docs/api_reference/trace.h.html
