========================
 List Output Formatters
========================

cliff-tablib delivers several new output formatters for list commands.

html
====

The ``html`` formatter uses tablib_ to produce HTML output as a table.

::

  (.venv)$ cliffdemo files -f html
  <table>
  <thead>
  <tr><th>Name</th>
  <th>Size</th></tr>
  </thead>
  <tr><td>build</td>
  <td>136</td></tr>
  <tr><td>cliffdemo.log</td>
  <td>3252</td></tr>
  <tr><td>Makefile</td>
  <td>5569</td></tr>
  <tr><td>requirements.txt</td>
  <td>33</td></tr>
  <tr><td>source</td>
  <td>782</td></tr>
  </table>

json
====

The ``json`` formatter uses tablib_ to produce JSON output.

::

  (.venv)$ cliffdemo files -f json
  [{"Name": "build", "Size": 136}, {"Name": "cliffdemo.log", "Size":
  3461}, {"Name": "Makefile", "Size": 5569}, {"Name":
  "requirements.txt", "Size": 33}, {"Name": "source", "Size": 782}]

yaml
====

The ``yaml`` formatter uses tablib_ to produce YAML output as a
sequence of mappings.

::

  (.venv)$ cliffdemo files -f yaml
  - {Name: build, Size: 136}
  - {Name: cliffdemo.log, Size: 3043}
  - {Name: Makefile, Size: 5569}
  - {Name: requirements.txt, Size: 33}
  - {Name: source, Size: 816}

.. _tablib: https://github.com/kennethreitz/tablib
