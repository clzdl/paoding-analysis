#Paoding分词器基于Lucene6.6.0
原作者： http://git.oschina.net/zhzhenqin/paoding-analysis 
原项目见 https://code.google.com/p/paoding/


#编译说明

项目默认可以使用Maven直接编译.

如果使用Ant,可把依赖的lib放入 {pro_workspace}/target/dependency/ 下. 然后使用ant可以直接编译.
编译的结果存放在 {pro_workspace}/target/dist/{version}/ 下


可使用Maven的 copy-dependencies 命令直接copy依赖到{pro_workspace}/target/dependency/，然后使用ant编译


    mvn dependency：copy-dependencies


#Solr4.x使用说明

Solr 4.x以上可以直接配置Lucene的Analyzer.
配置如:


    <fieldType name="text_general" class="solr.TextField">
      <analyzer class="net.paoding.analysis.analyzer.PaodingAnalyzer" />
    </fieldType>

