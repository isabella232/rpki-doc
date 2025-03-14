.. index:: ! Software Projects

.. _doc_tools:

Software Projects
=================

This section provides an overview of all well known open source projects that
support RPKI. It includes Relying Party software for validating RPKI data,
Certificate Authority software to run RPKI on your own infrastructure and
supporting tools that help deployment and integration.

.. index:: Relying Party software
  see: RPKI Validator; Relying Party software

.. _relying_party_software:

Relying Party Software
----------------------

.. csv-table:: 
   :header: "Name", "Maintainer", "Language", "Last Commit" 

   "`FORT Validator <https://github.com/NICMx/FORT-validator>`_ [#]_", "NIC.mx", "C", ".. image:: https://img.shields.io/github/last-commit/NICMx/FORT-validator?label=%20&style=flat-square"
   "`OctoRPKI <https://github.com/cloudflare/cfrpki#octorpki>`_", "Cloudflare", "Go", ".. image:: https://img.shields.io/github/last-commit/cloudflare/cfrpki?label=%20&style=flat-square"
   "`rcynic <https://github.com/dragonresearch/rpki.net>`_", "Dragon Research Labs", "Python 2", ".. image:: https://img.shields.io/github/last-commit/dragonresearch/rpki.net?label=%20&style=flat-square"   
   "`Routinator <https://github.com/NLnetLabs/routinator>`_", "NLnet Labs", "Rust", ".. image:: https://img.shields.io/github/last-commit/nlnetlabs/routinator?label=%20&style=flat-square"
   "`rpki-client <https://github.com/rpki-client/rpki-client-portable>`_", "OpenBSD", "C", ".. image:: https://img.shields.io/github/last-commit/rpki-client/rpki-client-portable?label=%20&style=flat-square"
   "`rpki-prover <https://github.com/lolepezy/rpki-prover>`_", "Misha Puzanov", "Haskell", ".. image:: https://img.shields.io/github/last-commit/lolepezy/rpki-prover?label=%20&style=flat-square"
   "`RPKI Validator <https://github.com/RIPE-NCC/rpki-validator-3>`_ [#]_", "RIPE NCC", "Java", ".. image:: https://img.shields.io/github/last-commit/RIPE-NCC/rpki-validator-3?label=%20&style=flat-square"
   "`RPSTIR2 <https://github.com/bgpsecurity/rpstir2>`_", "ZDNS", "Go", ".. image:: https://img.shields.io/github/last-commit/bgpsecurity/rpstir2?label=%20&style=flat-square"

.. [#] Due to a temporary resource shortage, the project’s development has slowed down to essential maintenance. `[Source] <https://nicmx.github.io/FORT-validator/>`_
.. [#] Discontinued on 1 July 2021. `[Source] <https://www.ripe.net/publications/news/announcements/ending-support-for-the-ripe-ncc-rpki-validator>`_

.. index:: RTR Server software

RTR Server Software
-------------------

.. csv-table:: 
   :header: "Name", "Maintainer", "Language", "Last Commit" 

   "`GoRTR <https://github.com/cloudflare/gortr>`_ [#]_", "Cloudflare", "Go", ".. image:: https://img.shields.io/github/last-commit/cloudflare/gortr?label=%20&style=flat-square"
   "`StayRTR <https://github.com/bgp/stayrtr/>`_ [#]_", "bgp", "Go", ".. image:: https://img.shields.io/github/last-commit/bgp/stayrtr?label=%20&style=flat-square"
   "`RTRTR <https://github.com/NLnetLabs/rtrtr>`_", "NLnet Labs", "Rust", ".. image:: https://img.shields.io/github/last-commit/nlnetlabs/rtrtr?label=%20&style=flat-square"
   "`rpkirtr <https://github.com/mellowdrifter/rpkirtr>`_", "Darren O'Connor", "Go", ".. image:: https://img.shields.io/github/last-commit/mellowdrifter/rpkirtr?label=%20&style=flat-square"

.. [#] Unmaintained since the developer got a new job. `[Source] <https://twitter.com/lpoinsig/status/1394144623489019904>`_
.. [#] A fork of GoRTR

.. index:: Certificate Authority software

Certificate Authority Software
------------------------------

.. csv-table:: 
   :header: "Name", "Maintainer", "Language", Last Commit 

   "`Krill <https://github.com/NLnetLabs/krill>`_", "NLnet Labs", "Rust", ".. image:: https://img.shields.io/github/last-commit/NLnetLabs/krill?label=%20&style=flat-square"
   "`rpkid <https://github.com/dragonresearch/rpki.net>`_", "Dragon Research Labs", "Python 2", ".. image:: https://img.shields.io/github/last-commit/dragonresearch/rpki.net?label=%20&style=flat-square"

Supporting Tools
----------------

`BGPalerter <https://github.com/nttgin/BGPalerter>`_
   A self-configuring BGP monitoring tool, which allows you to monitor in 
   real-time if any of your prefixes loses visibility or is hijacked, your AS is
   announcing RPKI invalid prefixes or is announcing prefixes not covered by 
   ROAs, ROAs covering your prefixes are no longer reachable, and much more. 
   
`BGP-SRx <https://www.nist.gov/services-resources/software/bgp-secure-routing-extension-bgp-srx-prototype>`_
   SRx is an open source reference implementation and research platform by the
   National Institute for Standards and Technology (NIST). It is intended for
   investigating emerging BGP security extensions and supporting protocols such
   as RPKI Origin Validation and BGPSec Path Validation.

`krill-sync <https://github.com/NLnetLabs/krill-sync>`_
   This tool uses the RRDP data from a (single) "hidden" backend RPKI
   Publication Server to make a consistent local copy of that data. This is
   intended to facilitate a redundant set up where one or more public https and
   rsync servers are used to make the RPKI repository content available.

`pmacct <http://pmacct.net>`_
   pmacct is a small set of multi-purpose passive network monitoring tools.
   It can account, classify, aggregate, replicate and export forwarding-plane
   data, i.e. IPv4 and IPv6 traffic; collect and correlate control-plane data
   via BGP and BMP; collect and correlate RPKI data; collect infrastructure
   data via Streaming Telemetry.

   The pmacct toolset can perform RPKI Origin Validation and present
   the outcome as a property in the flow aggregation process. Because it
   separates out the various types kinds of (invalid) BGP announcements,
   operators can a good grasp on how their connectivity to the rest of the
   Internet would look like after deploying a *"invalid == reject"* policy.

`rpki-ov-checker <https://github.com/job/rpki-ov-checker>`_
   rpki-ov-checker is an open source utility to quickly analyse BGP RIB dumps
   and the potential impact of deploying "invalid is reject" routing policies.

`RTRLib <https://github.com/rtrlib/rtrlib>`_
   The RTRlib implements the client-side of the RPKI-RTR protocol
   (:RFC:`6810`, :RFC:`8210`) and BGP Prefix Origin
   Validation (:RFC:`6811`). This also enables the maintenance of
   router keys, which are required to deploy BGPSec.
