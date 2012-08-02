========================
 Show Output Formatters
========================

cliff is delivered with output formatters for show
commands. :class:`ShowOne` adds a command line switch to let the user
specify the formatter they want, so you don't have to do any extra
work in your application.

html
----

The ``html`` formatter uses tablib_ to produce HTML output as a table.

::

    (.venv)$ cliffdemo file -f html setup.py
    <table>
    <thead>
    <tr><th>Field</th>
    <th>Value</th></tr>
    </thead>
    <tr><td>Name</td>
    <td>setup.py</td></tr>
    <tr><td>Size</td>
    <td>6373</td></tr>
    <tr><td>UID</td>
    <td>527</td></tr>
    <tr><td>GID</td>
    <td>501</td></tr>
    <tr><td>Modified Time</td>
    <td>1336353173.0</td></tr>
    </table>

json
----

The ``json`` formatter uses tablib_ to produce JSON output.

::

    (.venv)$ cliffdemo file -f json setup.py
    [{"Field": "Name", "Value": "setup.py"}, {"Field": "Size",
    "Value": 6373}, {"Field": "UID", "Value": 527}, {"Field": "GID",
    "Value": 501}, {"Field": "Modified Time", "Value": 1336353173.0}]

yaml
----

The ``yaml`` formatter uses tablib_ to produce YAML output as a
sequence of mappings.

::

    (.venv)$ cliffdemo file -f yaml setup.py
    - {Field: Name, Value: setup.py}
    - {Field: Size, Value: 6373}
    - {Field: UID, Value: 527}
    - {Field: GID, Value: 501}
    - {Field: Modified Time, Value: 1336353173.0}


.. _tablib: https://github.com/kennethreitz/tablib
