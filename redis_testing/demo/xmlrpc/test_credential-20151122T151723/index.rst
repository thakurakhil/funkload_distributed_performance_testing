======================
FunkLoad_ bench report
======================


:date: 2015-11-22 15:17:23
:abstract: Try to test all xml rpc method
           Bench result of ``Credential.test_credential``: 
           Check all credentiald methods

.. _FunkLoad: http://funkload.nuxeo.org/
.. sectnum::    :depth: 2
.. contents:: Table of contents
.. |APDEXT| replace:: \ :sub:`1.5`

Bench configuration
-------------------

* Launched: 2015-11-22 15:17:23
* From: vijay-VirtualBox
* Test: ``test_Credential.py Credential.test_credential``
* Target server: http://localhost:44401/
* Cycles of concurrent users: [1, 20, 40, 60, 80, 100]
* Cycle duration: 10s
* Sleeptime between request: from 0.1s to 0.2s
* Sleeptime between test case: 0.5s
* Startup delay between thread: 0.05s
* Apdex: |APDEXT|
* FunkLoad_ version: 1.16.1


Bench content
-------------

The test ``Credential.test_credential`` contains: 

* 0 page(s)
* 0 redirect(s)
* 0 link(s)
* 0 image(s)
* 5 XML RPC call(s)

The bench contains:

* 2193 tests
* 10888 pages
* 10888 requests


Test stats
----------

The number of Successful **Tests** Per Second (STPS) over Concurrent Users (CUs).

 .. image:: tests.png

 ================== ================== ================== ================== ==================
                CUs               STPS              TOTAL            SUCCESS              ERROR
 ================== ================== ================== ================== ==================
                  1              0.800                  8                  8             0.00%
                 20             15.800                158                158             0.00%
                 40             31.700                317                317             0.00%
                 60             48.000                480                480             0.00%
                 80             55.100                551                551             0.00%
                100             67.900                679                679             0.00%
 ================== ================== ================== ================== ==================



Page stats
----------

The number of Successful **Pages** Per Second (SPPS) over Concurrent Users (CUs).
Note that an XML RPC call count like a page.

 .. image:: pages_spps.png
 .. image:: pages.png

 ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================
                CUs             Apdex*             Rating               SPPS            maxSPPS              TOTAL            SUCCESS              ERROR                MIN                AVG                MAX                P10                MED                P90                P95
 ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================
                  1              1.000          Excellent              4.000              5.000                 40                 40             0.00%              0.001              0.003              0.005              0.001              0.003              0.004              0.004
                 20              1.000          Excellent             79.000             85.000                790                790             0.00%              0.001              0.002              0.016              0.001              0.001              0.004              0.006
                 40              1.000          Excellent            158.400            169.000               1584               1584             0.00%              0.000              0.002              0.205              0.001              0.001              0.003              0.005
                 60              1.000          Excellent            237.000            247.000               2370               2370             0.00%              0.000              0.002              0.012              0.001              0.001              0.003              0.005
                 80              0.998          Excellent            272.800            318.000               2728               2728             0.00%              0.000              0.042              3.010              0.001              0.002              0.012              0.032
                100              0.999          Excellent            337.600            385.000               3376               3376             0.00%              0.000              0.048              3.414              0.001              0.002              0.013              0.037
 ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================

 \* Apdex |APDEXT|

Request stats
-------------

The number of **Requests** Per Second (RPS) successful or not over Concurrent Users (CUs).

 .. image:: requests_rps.png
 .. image:: requests.png

 ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================
                CUs             Apdex*            Rating*                RPS             maxRPS              TOTAL            SUCCESS              ERROR                MIN                AVG                MAX                P10                MED                P90                P95
 ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================
                  1              1.000          Excellent              4.000              5.000                 40                 40             0.00%              0.001              0.003              0.005              0.001              0.003              0.004              0.004
                 20              1.000          Excellent             79.000             85.000                790                790             0.00%              0.001              0.002              0.016              0.001              0.001              0.004              0.006
                 40              1.000          Excellent            158.400            169.000               1584               1584             0.00%              0.000              0.002              0.205              0.001              0.001              0.003              0.005
                 60              1.000          Excellent            237.000            247.000               2370               2370             0.00%              0.000              0.002              0.012              0.001              0.001              0.003              0.005
                 80              0.998          Excellent            272.800            318.000               2728               2728             0.00%              0.000              0.042              3.010              0.001              0.002              0.012              0.032
                100              0.999          Excellent            337.600            385.000               3376               3376             0.00%              0.000              0.048              3.414              0.001              0.002              0.013              0.037
 ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================

 \* Apdex |APDEXT|

Slowest requests
----------------

The 5 slowest average response time during the best cycle with **100** CUs:

* In page 003, Apdex rating: Excellent, avg response time: 0.06s, xmlrpc: ``http://localhost:44401/#listGroups``
  `list groups from the group file`
* In page 001, Apdex rating: Excellent, avg response time: 0.05s, xmlrpc: ``http://localhost:44401/#getStatus``
  `Check getStatus`
* In page 005, Apdex rating: Excellent, avg response time: 0.05s, xmlrpc: ``http://localhost:44401/#listCredentials``
  `list credentials of group AdminZope`
* In page 004, Apdex rating: Excellent, avg response time: 0.04s, xmlrpc: ``http://localhost:44401/#listCredentials``
  `list all credential of the file`
* In page 002, Apdex rating: Excellent, avg response time: 0.04s, xmlrpc: ``http://localhost:44401/#getCredential``
  `Get a credential from a file`

Page detail stats
-----------------


PAGE 001: Check getStatus
~~~~~~~~~~~~~~~~~~~~~~~~~

* Req: 001, xmlrpc, url ``http://localhost:44401/#getStatus``

     .. image:: request_001.001.png

     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================
                    CUs             Apdex*             Rating              TOTAL            SUCCESS              ERROR                MIN                AVG                MAX                P10                MED                P90                P95
     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================
                      1              1.000          Excellent                  8                  8             0.00%              0.001              0.003              0.004              0.001              0.003              0.004              0.004
                     20              1.000          Excellent                157                157             0.00%              0.001              0.002              0.010              0.001              0.001              0.003              0.005
                     40              1.000          Excellent                318                318             0.00%              0.000              0.002              0.022              0.001              0.001              0.003              0.005
                     60              1.000          Excellent                472                472             0.00%              0.000              0.002              0.011              0.001              0.001              0.003              0.005
                     80              0.997          Excellent                542                542             0.00%              0.001              0.041              3.006              0.001              0.002              0.012              0.024
                    100              0.999          Excellent                674                674             0.00%              0.000              0.052              3.011              0.001              0.002              0.016              0.198
     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================

     \* Apdex |APDEXT|

PAGE 002: Get a credential from a file
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Req: 001, xmlrpc, url ``http://localhost:44401/#getCredential``

     .. image:: request_002.001.png

     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================
                    CUs             Apdex*             Rating              TOTAL            SUCCESS              ERROR                MIN                AVG                MAX                P10                MED                P90                P95
     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================
                      1              1.000          Excellent                  8                  8             0.00%              0.001              0.003              0.005              0.001              0.003              0.005              0.005
                     20              1.000          Excellent                158                158             0.00%              0.001              0.002              0.016              0.001              0.001              0.005              0.007
                     40              1.000          Excellent                318                318             0.00%              0.000              0.003              0.205              0.001              0.001              0.003              0.004
                     60              1.000          Excellent                478                478             0.00%              0.000              0.002              0.012              0.001              0.001              0.003              0.005
                     80              0.999          Excellent                545                545             0.00%              0.000              0.039              3.005              0.001              0.002              0.012              0.031
                    100              0.999          Excellent                673                673             0.00%              0.000              0.038              3.208              0.001              0.002              0.012              0.018
     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================

     \* Apdex |APDEXT|

PAGE 003: list groups from the group file
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Req: 001, xmlrpc, url ``http://localhost:44401/#listGroups``

     .. image:: request_003.001.png

     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================
                    CUs             Apdex*             Rating              TOTAL            SUCCESS              ERROR                MIN                AVG                MAX                P10                MED                P90                P95
     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================
                      1              1.000          Excellent                  8                  8             0.00%              0.001              0.002              0.003              0.001              0.003              0.003              0.003
                     20              1.000          Excellent                156                156             0.00%              0.001              0.002              0.008              0.001              0.001              0.004              0.005
                     40              1.000          Excellent                313                313             0.00%              0.000              0.002              0.018              0.001              0.001              0.003              0.004
                     60              1.000          Excellent                472                472             0.00%              0.000              0.002              0.011              0.001              0.001              0.004              0.005
                     80              0.999          Excellent                546                546             0.00%              0.000              0.044              3.005              0.001              0.002              0.012              0.026
                    100              0.999          Excellent                678                678             0.00%              0.000              0.061              3.015              0.001              0.002              0.014              0.218
     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================

     \* Apdex |APDEXT|

PAGE 004: list all credential of the file
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Req: 001, xmlrpc, url ``http://localhost:44401/#listCredentials``

     .. image:: request_004.001.png

     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================
                    CUs             Apdex*             Rating              TOTAL            SUCCESS              ERROR                MIN                AVG                MAX                P10                MED                P90                P95
     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================
                      1              1.000          Excellent                  8                  8             0.00%              0.002              0.003              0.004              0.002              0.003              0.004              0.004
                     20              1.000          Excellent                159                159             0.00%              0.001              0.003              0.016              0.001              0.002              0.005              0.008
                     40              1.000          Excellent                317                317             0.00%              0.001              0.002              0.021              0.001              0.001              0.004              0.005
                     60              1.000          Excellent                475                475             0.00%              0.000              0.002              0.012              0.001              0.001              0.004              0.004
                     80              0.999          Excellent                546                546             0.00%              0.000              0.041              3.005              0.001              0.002              0.013              0.035
                    100              0.999          Excellent                672                672             0.00%              0.000              0.039              3.017              0.001              0.002              0.011              0.022
     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================

     \* Apdex |APDEXT|

PAGE 005: list credentials of group AdminZope
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Req: 001, xmlrpc, url ``http://localhost:44401/#listCredentials``

     .. image:: request_005.001.png

     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================
                    CUs             Apdex*             Rating              TOTAL            SUCCESS              ERROR                MIN                AVG                MAX                P10                MED                P90                P95
     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================
                      1              1.000          Excellent                  8                  8             0.00%              0.001              0.002              0.004              0.001              0.003              0.004              0.004
                     20              1.000          Excellent                160                160             0.00%              0.001              0.002              0.012              0.001              0.001              0.005              0.006
                     40              1.000          Excellent                318                318             0.00%              0.000              0.002              0.016              0.001              0.001              0.003              0.005
                     60              1.000          Excellent                473                473             0.00%              0.000              0.002              0.009              0.001              0.001              0.004              0.004
                     80              0.996          Excellent                549                549             0.00%              0.001              0.044              3.010              0.001              0.002              0.013              0.054
                    100              0.999          Excellent                679                679             0.00%              0.000              0.051              3.414              0.001              0.002              0.013              0.200
     ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ================== ==================

     \* Apdex |APDEXT|

Definitions
-----------

* CUs: Concurrent users or number of concurrent threads executing tests.
* Request: a single GET/POST/redirect/xmlrpc request.
* Page: a request with redirects and resource links (image, css, js) for an html page.
* STPS: Successful tests per second.
* SPPS: Successful pages per second.
* RPS: Requests per second, successful or not.
* maxSPPS: Maximum SPPS during the cycle.
* maxRPS: Maximum RPS during the cycle.
* MIN: Minimum response time for a page or request.
* AVG: Average response time for a page or request.
* MAX: Maximmum response time for a page or request.
* P10: 10th percentile, response time where 10 percent of pages or requests are delivered.
* MED: Median or 50th percentile, response time where half of pages or requests are delivered.
* P90: 90th percentile, response time where 90 percent of pages or requests are delivered.
* P95: 95th percentile, response time where 95 percent of pages or requests are delivered.
* Apdex T: Application Performance Index, 
  this is a numerical measure of user satisfaction, it is based
  on three zones of application responsiveness:

  - Satisfied: The user is fully productive. This represents the
    time value (T seconds) below which users are not impeded by
    application response time.

  - Tolerating: The user notices performance lagging within
    responses greater than T, but continues the process.

  - Frustrated: Performance with a response time greater than 4*T
    seconds is unacceptable, and users may abandon the process.

    By default T is set to 1.5s this means that response time between 0
    and 1.5s the user is fully productive, between 1.5 and 6s the
    responsivness is tolerating and above 6s the user is frustrated.

    The Apdex score converts many measurements into one number on a
    uniform scale of 0-to-1 (0 = no users satisfied, 1 = all users
    satisfied).

    Visit http://www.apdex.org/ for more information.
* Rating: To ease interpretation the Apdex
  score is also represented as a rating:

  - U for UNACCEPTABLE represented in gray for a score between 0 and 0.5 

  - P for POOR represented in red for a score between 0.5 and 0.7

  - F for FAIR represented in yellow for a score between 0.7 and 0.85

  - G for Good represented in green for a score between 0.85 and 0.94

  - E for Excellent represented in blue for a score between 0.94 and 1.

Report generated with FunkLoad_ 1.16.1, more information available on the `FunkLoad site <http://funkload.nuxeo.org/#benching>`_.