Elasticsearch munin plugins
==========================================================

elasticsearch_cluster_*のプラグインは

http://127.0.0.1:9200/_cluster/stats

で取得できるjsonからmunin用にスクリプトを作りました.

elasticsearch_node_*のプラグインは

http://127.0.0.1:9200/_nodes/ノードネーム

で取得できるjsonからmunin用にスクリプトを作りました.


====

.. contents::

====

設定方法
-------
CentOS6.4でelasticsearch-1.0.1-1.noarchで検証済みです.
他のOSはサポートしてません.(未検証)

* git clone git@github.com:editnuki/elasticsearch-munin-plugins.git
* cd elasticsearch-munin-plugins/plugins
* cp elasticsearch-* /usr/share/munin/plugins/
* ln -s /usr/share/munin/plugins/elasticsearch-* /etc/munin/plugins/

* ``node.name`` はhostnameコマンドで取得できるホスト名で決め打ちにしてしまっています

Changelog
---------

1.0.1
`````

 * delete plugin-conf.d

 * plugin-conf.dに設定しなくても各ノードのグラフが取得できるようになりました

1.0.0
`````

 * add node plugins


0.0.2
`````

 * add plugins

 * jvm heap_used and file_descriptors

0.0.1
`````

 * create first
