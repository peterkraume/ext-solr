.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. include:: ../../Includes.txt


.. _typoscript:

TypoScript
==========

.. important:: All setting needs to be prefixed with :typoscript:`plugin.`.

.. only:: html

   .. contents::
        :local:
        :depth: 1


tx_solr
-------

This section defines general configuration options.

Properties
^^^^^^^^^^

.. container:: ts-properties

	==================================== ===============
	Property                             Type
	==================================== ===============
	enabled_                              boolean
	addDefaultCss_                        boolean
	addDefaultJs_                         boolean
	enableDebugMode_                      boolean
	==================================== ===============

.. _tsEnabled:

enabled
"""""""
.. container:: table-row

   Property
         enabled
   Data type
         boolean
   Description
         A switch to completely turn on / off EXT:solr. Comes in handy with multi site installations where you want to enable EXT:solr only for certain sites, but still have the extension's configuration at a single place and include that for each site. Just set :typoscript:`enabled = 0` for each site's root TS template or use conditions where you do not want EXT:solr.

         .. important:: This also influences the connection manager, connections will be registered / detected only for :typoscript:`enabled = 1`.
   Since:
         1.2
   Default:
         1
   Options:
         0, 1

.. _tsAddDefaultCss:

addDefaultCss
"""""""""""""
.. container:: table-row

   Property
         addDefaultCss
   Data type
         boolean
   Description
         If enabled, default stylesheets for page browser, results, and suggestions will be included. Otherwise, no stylesheets will be included by EXT:solr.
   Since:
         1.0
   Removed:
         2.0, see  :ref:`tx_solr.cssFiles` instead
   Default:
         1
   Options:
         0, 1

.. _tsAddDefaultJs:

addDefaultJs
""""""""""""
.. container:: table-row

   Property
         addDefaultJs
   Data type
         boolean
   Description
         If enabled, some javascript files for facet option (un)folding and suggestions will be included. Furthermore, the jQuery UI library required for suggestions can only get included, if addDefaultJs is set.
   Since:
         1.0
   Removed:
         2.0, see  :ref:`tx_solr.javascriptFiles` instead
   Default:
         1
   Options:
         0, 1

.. _tsEnableDebugMode:

enableDebugMode
"""""""""""""""
.. container:: table-row

   Property
         enableDebugMode
   Data type
         boolean
   Description
         If enabled, the *debugQuery* query parameter is added to the Solr queries. Solr will then return additional information explaining the the query, scoring, timing, and other information.
   Since:
         1.0
   Default:
         1
   Options:
         0, 1
   See:
         http://wiki.apache.org/solr/CommonQueryParameters#debugQuery

tx_solr.general
---------------

This section defines general settings.

Properties
^^^^^^^^^^

.. container:: ts-properties

	==================================== ===============
	Property                             Type
	==================================== ===============
	dateFormat.date_                      string
	==================================== ===============

.. _tsGeneralDateFormat.date:

dateFormat.date
"""""""""""""""
.. container:: table-row

   Property
         dateFormat.date
   Data type
         string
   Description
         Defines the format that is used for dates throughout the extension like in viewhelpers for example. The format uses the strftime() php function syntax, please consult the php documentation for available options.
   Since:
         1.0
   Default:
         d.m.Y H:i
   See:
         http://de.php.net/manual/de/function.strftime.php


tx_solr.solr
------------


tx_solr.templateFiles
---------------------

.. _tx_solr.cssFiles:

tx_solr.cssFiles
----------------

.. _tx_solr.javascriptFiles:

tx_solr.javascriptFiles
-----------------------


tx_solr.index
-------------


tx_solr.search
--------------


tx_solr.suggest
---------------


tx_solr.moreLikeThis
--------------------


tx_solr.statistics
------------------


tx_solr.viewhelpers
-------------------


tx_solr.logging
---------------
