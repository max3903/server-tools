.. image:: https://img.shields.io/badge/licence-AGPL--3-blue.svg
   :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
   :alt: License: AGPL-3

==========================
Key Performance Indicators
==========================

This module provides the basis for creating key performance indicators,
including static and dynamic thresholds (SQL query or Python code),
on local and remote data sources.

The module also provides the mechanism to update KPIs automatically.
A scheduler is executed every hour and updates the KPI values, based
on the periodicity of each KPI. KPI computation can also be done
manually.

A threshold is a list of ranges and a range is:

* a name (like Good, Warning, Bad)
* a minimum value (fixed, sql query or python code)
* a maximum value (fixed, sql query or python code)
* a color (RGB code like #00FF00 for green, #FFA500 for orange, #FF0000 for
red)

Installation
============

If you want to compute KPI from an external database, you will need to
install the python library for that database.

Depending on the database, you need:
 * to install unixodbc and python-pyodbc packages to use ODBC connections.
 * to install FreeTDS driver (tdsodbc package) and configure it through ODBC to
   connect to Microsoft SQL Server.
 * to install and configure Oracle Instant Client and cx_Oracle python library
   to connect to Oracle.

Configuration
=============

* Database sources can be configured in Settings > Technical > Database
  Structure > Data Sources
* To configure KPI, watch https://www.youtube.com/watch?v=OC4-y2klzIk

Usage
=====

* Go to Dashboard > Dashboard > KPI to see the state of your KPI

.. image:: https://odoo-community.org/website/image/ir.attachment/5784_f2813bd/datas
   :alt: Try me on Runbot
   :target: https://runbot.odoo-community.org/runbot/149/9.0

Known issues / Roadmap
======================

* Use web_widget_color to display color associated to threshold range

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/server-tools/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and welcomed feedback `here <https://github.com/OCA/
server-tools/issues/new?body=module:%20
kpi%0Aversion:%20
9.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Credits
=======

Contributors
------------

* Daniel Reis <dreis.pt@hotmail.com>
* Glen Dromgoole <gdromgoole@tier1engineering.com>
* Loic Lacroix <loic.lacroix@savoirfairelinux.com>
* Sandy Carter <sandy.carter@savoirfairelinux.com>
* Gervais Naoussi <gervaisnaoussi@gmail.com>
* Maxime Chambreuil <mchambreuil@ursainfosystems.com>

Maintainer
----------

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

This module is maintained by the OCA.

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

To contribute to this module, please visit http://odoo-community.org.
