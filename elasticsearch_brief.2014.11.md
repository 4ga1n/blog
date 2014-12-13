# Elasticsearch 2014年11月简报

---

## TODO
*	Amazing Slides写介绍
*	

## Elasticsearch Updates
*	Elasticsearch 1.4.0发布了，最新最稳定的版本。
这个版本主要加强了Es的稳定性和可靠性，内存管理更合理，加入数据校验以发现损坏的数据。
	*    Doc values (fielddata written to disk at index time) greatly reduces heap usage.
	*    Request circuit breaker to abort search requests which consume too much memory.
	*    Bloom filters are disabled by default as they are no longer needed for fast indexing.
	*    Increased use of checksums to detect data corruption early.
	*    Groovy replaces MVEL as the default scripting language.
	*    CORS is disabled by default to prevent XSS attacks.
	*    Query cache to return aggregation results instantly on shards that have not changes.
	*    New aggregations: filters (docs), children (docs), and scripted_metric (docs).
	*    A new GET /index API which returns index settings, mappings, warmers, and aliases in a single request (docs).
	*    Flake IDs for auto-generated document IDs, which improve primary key lookup performance.
	*    Updates which don’t make any change to the document can avoid reindexing the document.
	*    Functions in the function_score query can be individually tuned with the weight parameter (docs).

我在[10月的Es简报中发布了Elasticsearch 1.4.0.Beta1](https://github.com/garyelephant/blog/blob/master/elasticsearch_brief.2014.10.md)中提到了更详细的变化。

## Elasticsearch Ecosystem Updates
*	elasticsearch背后的公司elasticsearch.com即将在年底发布一款重量级产品：[Shield ](http://www.elasticsearch.org/overview/shield/)(elasticsearch的神盾特工局，专门保护elasticsearch的安全)。Shield预计是以elasticsearch插件的方式集成到其中。相信感受过此公司的[Marvel](http://www.elasticsearch.org/overview/marvel/)易用性的用户应该会很期待这款产品。Shield主要提供了4个功能：
	*    基于用户角色对Index读、写、查询的权限控制
	*    对基于LDAP和Active Directory验证的支持
	*    使用SSL/TLS对es node之间，client和node之间的传输加密
	*     记录安全相关的日志
详情见：[shield: you know, for security](http://www.elasticsearch.org/blog/shield-know-security-coming-soon/)

*	kibana 4 beta 2发布了
	*    现在支持地图了，利用aggregations在地图上地理位置相关的数据。
![Kibana4 beta 2 map support](https://github.com/garyelephant/blog/blob/master/images/elasticsearch_brief_2014.11_kibana_map_support.png)
	*    条形图可以以独立的方式按组绘制了，如在一个数据点上的html,css,php.这正是我们需要的功能。
![Kibana4 beta 2 group bar chart](https://github.com/garyelephant/blog/blob/master/images/elasticsearch_brief_2014.11_kibana_group_bar_chart.png)
	*     朴素的数据表，只展示数据
![Kibana4 beta 2 data table](https://github.com/garyelephant/blog/blob/master/images/elasticsearch_brief_2014.11_kibana_data_table.png)
	*    

## Amazing Slides & tutorials & videos
*	[migrating his Elasticsearch cluster from Canada to France with zero downtime](https://t37.net/migrate-your-es-cluster-from-one-continent-to-another-without-downtime.html)
*	[Having Fun: Python and Elasticsearch, Part 1](http://bitquabit.com/post/having-fun-python-and-elasticsearch-part-1/)使用python入门Elasticsearch 

## Meetups in China


##References
1. shield: you know, for security http://www.elasticsearch.org/blog/shield-know-security-coming-soon/ 
2. Elasticsearch 1.4.0 and 1.3.5 released http://www.elasticsearch.org/blog/elasticsearch-1-4-0-released/
3. This week in ElasticsearchNovember 5, 2014 http://www.elasticsearch.org/blog/2014-11-05-this-week-in-elasticsearch/
4. This week in ElasticsearchNovember 12, 2014 http://www.elasticsearch.org/blog/2014-11-12-this-week-in-elasticsearch/
5. kibana 4 beta 2: get it now http://www.elasticsearch.org/blog/kibana-4-beta-2-get-now/


---

ES Updates:
*	http://www.elasticsearch.org/blog/elasticsearch-1-4-0-released/ "elasticsearch 1.4.0 and 1.3.5 released"
*	http://www.elasticsearch.org/blog/2014-11-05-this-week-in-elasticsearch/ "This week in ElasticsearchNovember 5, 2014"
*	http://www.elasticsearch.org/blog/2014-11-12-this-week-in-elasticsearch/ "This week in ElasticsearchNovember 12, 2014"
*	http://www.elasticsearch.org/blog/2014-11-1-this-week-in-elasticsearch/ "This Week in ElasticsearchNovember 19, 2014"
*	http://www.elasticsearch.org/blog/2014-11-26-this-week-in-elasticsearch/ "This week in elasticsearchNovember 26, 2014"
*	http://www.elasticsearch.org/blog/elasticsearch-1-4-1-released/ "http://www.elasticsearch.org/blog/2014-11-26-this-week-in-elasticsearch/"
*	http://www.elasticsearch.org/blog/making-elasticsearch-groovy-er/ "Making Elasticsearch Groovy-er"

Ecosystem:
*	http://www.elasticsearch.org/blog/shield-know-security-coming-soon/ "shield: you know, for security (coming soon)"
*	 http://www.elasticsearch.org/blog/kibana-4-beta-2-get-now/ "Kibana 4 Beta 2: Get it nowNovember 11, 2014"
*	http://www.elasticsearch.org/blog/elasticsearch-yarn-and-ssl/ "Elasticsearch on YARN and SSL support in Elasticsearch Hadoop"

Amazing tutorials & slides
*	http://www.elasticsearch.org/blog/white-paper-testing-automation-for-distributed-applications/ "White Paper: Testing Automation for Distributed Applications"
*	http://www.elasticsearch.org/blog/making-elasticsearch-groovy-er/ "Making Elasticsearch Groovy-er"


> Written with [StackEdit](https://stackedit.io/).