Elasticsearch munin plugins
==========================================================

http://127.0.0.1:9200/_cluster/stats?human&pretty
で取得できるjsonからmunin用にスクリプトを作りました.



====

.. contents::

====

設定方法
-------
CentOS6.4で検証済みです.
他のOSはサポートしてません.

* git clone git@github.com:editnuki/elasticsearch-munin-plugins.git
* cd elasticsearch-munin-plugins/plugins
* cp elasticsearch-* /usr/share/munin/plugins/
* ln -s /usr/share/munin/plugins/elasticsearch-* /etc/munin/plugins/

Changelog
---------

0.0.2
`````

 * add plugins
   * jvm heap_used and file_descriptors

0.0.1
`````

 * create first
