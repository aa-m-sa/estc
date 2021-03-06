---
title: "Preprocessing Summary"
author: "Leo Lahti"
date: "16/05/2015"
output: markdown_document
---

# Summary of the preprocessed ESTC data

## Field conversions

This document links to files that summarize the conversions from raw data to the final preprocessed version (accepted, discarded, conversions). Only some of the key tables are explicitly linked below. The complete list of those summary tables is available [here](output.tables/).









## Annotated documents

Fraction of documents with entries for each annotation field (final preprocessed data).

![plot of chunk summaryannotations](figure/summaryannotations-1.png)

Number of documents with NA entries (number and percentage) and number of unique entries for each field:


|                      |  docs| percentage| unique|
|:---------------------|-----:|----------:|------:|
|volnumber             |   156|  0.0031028|     15|
|author_birth          | 15486|  0.3080136|    351|
|author_death          | 16029|  0.3188138|    370|
|author_gender         | 16900|  0.3361378|      3|
|author_name           | 18232|  0.3626310|   6098|
|author_unique         | 18232|  0.3626310|   6451|
|topic                 | 21965|  0.4368797|   7065|
|publisher             | 40125|  0.7980786|  20782|
|latitude              | 44950|  0.8940470|    132|
|longitude             | 44950|  0.8940470|    132|
|paper.consumption.km2 | 48056|  0.9558247|   2814|
|width                 | 48091|  0.9565209|     52|
|height                | 48091|  0.9565209|     47|
|area                  | 48091|  0.9565209|    299|
|publication_country   | 48350|  0.9616723|     32|
|pagecount.orig        | 48679|  0.9682161|    938|
|publication_place     | 49786|  0.9902341|    410|
|publication_decade    | 49888|  0.9922629|     43|
|publication_year      | 49913|  0.9927601|    327|
|volcount              | 50121|  0.9968972|    109|
|pagecount             | 50232|  0.9991050|    997|
|language              | 50270|  0.9998608|     21|
|row.index             | 50277|  1.0000000|  50277|
|original_row          | 50277|  1.0000000|  50277|
|title                 | 50277|  1.0000000|  41289|
|gatherings            | 50277|  1.0000000|     16|
|obl                   | 50277|  1.0000000|      2|
|unity                 | 50277|  1.0000000|      1|


## Topics




Top-20 topics and number of documents for each. In total, there are 7065 unique topics and 21965 documents assigned to one or more topics (44).

![plot of chunk summarytopics22](figure/summarytopics22-1.png)


## Authors

[Discarded author names](output.tables/author_name_discarded.csv)

[Discarded author first names](output.tables/author_name_discarded_first.csv)

[Discarded author last names](output.tables/author_name_discarded_last.csv)


Top-20 uniquely identified authors and number of documents for each (duplicate docs not checked yet). In total, there are 6451 unique authors and 18232 documents with unambiguous author information (36%).


![plot of chunk summaryauthors](figure/summaryauthors-1.png)



### Gender

[Author genders](output.tables/author_gender_accepted.csv)

[Male authors](output.tables/gender_male.csv)

[Female authors](output.tables/gender_male.csv)

[Names with missing gender](output.tables/gender_unknown.csv)


Author gender distribution in the complete data:


|author_gender |  docs| fraction|
|:-------------|-----:|--------:|
|female        |   475|     0.94|
|male          | 16425|    32.67|
|NA            | 33377|    66.39|

Author gender distribution over time. Note that the name-gender mappings change over time. This has not been taken into account yet.


![plot of chunk summarygendertime](figure/summarygendertime-1.png)



### Ambiguous authors

Authors with ambiguous living year information - can we spot here
cases where these are clearly known identical or distinct authors?
Should also add living year information from supporting sources later.

[Authors with ambiguous life years](output.tables/author_life_ambiguous.csv)

[Authors with discarded life years](output.tables/author_life_discarded.csv)

[Authors with missing life years](output.tables/author_birth_unknown.csv)


### Life span of uniquely identified top authors

Ordered by productivity (number of documents))

![plot of chunk summaryauthorslife](figure/summaryauthorslife-1.png)

### Publication timeline for top-10 authors

Title count

![plot of chunk summaryTop10authorstimeline](figure/summaryTop10authorstimeline-1.png)


Paper consumption

![plot of chunk summaryTop10authorstimelinepaper](figure/summaryTop10authorstimelinepaper-1.png)




## Publication 

### Publication places

[Publication countries](output.tables/publication_country_accepted.csv)

[Publication country missing](output.tables/publication_country_discarded.csv)

[Discarded publication places](output.tables/publication_place_discarded.csv)

[Publication place conversions](output.tables/publication_place_conversions_nontrivial.csv)

[Places missing geocoordinate information](output.tables/absentgeocoordinates.csv)


Top-20 publication places are shown together with the number of documents. This info is available for 49786 documents (99%). There are 410 unique publication places. Overall 89.4% of the places could be matched to geographic coordinates (from the [Geonames](http://download.geonames.org/export/dump/) database).


![plot of chunk summaryplace](figure/summaryplace-1.png)



|            |     n|
|:-----------|-----:|
|England     | 38525|
|Ireland     |  3501|
|Scotland    |  2863|
|USA         |  2519|
|Netherlands |   309|
|France      |   300|
|Germany     |    58|
|Canada      |    52|
|Switzerland |    45|
|Belgium     |    43|
|India       |    40|
|Jamaica     |    25|
|Northern    |    10|
|Barbados    |    10|
|Saint       |     9|
|Italy       |     9|
|Bahamas     |     6|
|Dominica    |     4|
|Haiti       |     3|
|Guadaloupe  |     3|
|Denmark     |     3|
|Sweden      |     2|
|Spain       |     2|
|Austria     |     2|
|Walkes      |     1|
|unknown     |     1|
|Russia      |     1|
|Poland      |     1|
|Guernesey   |     1|
|Grenada     |     1|
|Europe      |     1|


### Publishers

[Publishers accepted](output.tables/publisher_accepted.csv)

[Publishers discarded](output.tables/publisher_discarded.csv)




The 20 most common publishers are shown with the number of documents. Publisher information is available for 40125 documents (80%). There are 20781 unique publisher names (some may be synonymes, though).


![plot of chunk summarypublisher2](figure/summarypublisher2-1.png)


### Publication timeline for top-10 publishers

Title count

![plot of chunk summaryTop10publisherstimeline](figure/summaryTop10publisherstimeline-1.png)


Paper consumption

![plot of chunk summaryTop10publisherstimelinepaper](figure/summaryTop10publisherstimelinepaper-1.png)


### Publication year


[Publication year conversions](output.tables/publication_year_conversion_table.csv)

[Publication year discarded](output.tables/publication_year_failed.csv)

Publication year is available for 49913 documents (99%). The publication years span 0-1799

![plot of chunk summarypublicationyear](figure/summarypublicationyear-1.png)

Zooming in 1470-1799

![plot of chunk summarypublicationyear2](figure/summarypublicationyear2-1.png)


### Titles

[Publication titles](output.tables/title_accepted.csv)

[Publication titles discarded](output.tables/title_discarded.csv)

[Title harmonization table](output.tables/title_conversions_nontrivial.csv)

Top-20 titles are shown together with the number of documents. This info is available for 50277 documents (100%). There are 41289 unique titles.


![plot of chunk summarytitle](figure/summarytitle-1.png)


## Language

The 21 unique languages are shown together with the number of documents. This info is available for 50270 documents (100%). 

![plot of chunk summarylang](figure/summarylang-1.png)



## Page counts

[Page conversions from raw data to final page count estimates](https://raw.githubusercontent.com/rOpenGov/estc/master/inst/examples/output.tables/page_conversion_table_brief.csv)

[Page conversions from raw data to final page count estimates with volume info](https://raw.githubusercontent.com/rOpenGov/estc/master/inst/examples/output.tables/page_conversion_table_full.csv)

[Discarded page info](https://raw.githubusercontent.com/rOpenGov/estc/master/inst/examples/output.tables/documentpages-discarded.csv)



## Document size comparisons

[Discarded dimension info](https://raw.githubusercontent.com/rOpenGov/estc/master/inst/examples/output.tables/dimensions_discarded.csv)

[Dimension conversion table](https://raw.githubusercontent.com/rOpenGov/estc/master/inst/examples/output.tables/dimension_conversion_table.csv)


Document size (area) info in area is available for 48091 documents (96%). Estimates of document size (area) info in gatherings system are available for 50277 documents (100%). 

![plot of chunk summarysize](figure/summarysize-1.png)

Compare gatherings and area sizes as a quality check. This includes all data; the area has been estimated from the gatherings when dimension information was not available.

![plot of chunk summarysizecomp](figure/summarysizecomp-1.png)

Document dimension histogram (surface area). Few document sizes dominate publishing.

![plot of chunk summary-surfacearea](figure/summary-surfacearea-1.png)



Compare gatherings and page counts. Page count information is estimated for -1553 documents and updated (changed) for 1093 documents. 

![plot of chunk summarypagecomp](figure/summarypagecomp-1.png)

Compare original gatherings and original heights where both are available. The point size indicates the number of documents with the corresponding combination. The red dots indicate the estimated height that is used when only gathering information is available. It seems that in most documents, the given height is smaller than the correponding estimate.

![plot of chunk summarysizevalidation](figure/summarysizevalidation-1.png)

## Average page counts 

Multi-volume documents average page counts are given per volume.


|doc.dimension | mean.pages.singlevol| median.pages.singlevol| n.singlevol| mean.pages.multivol| median.pages.multivol| n.multivol| mean.pages.issue| median.pages.issue| n.issue|
|:-------------|--------------------:|----------------------:|-----------:|-------------------:|---------------------:|----------:|----------------:|------------------:|-------:|
|1to           |             2.482172|                      2|        4249|                  NA|                    NA|         NA|         10.43590|                  8|      39|
|2long         |             7.714286|                      5|           8|                  NA|                    NA|         NA|         23.00000|                 23|       1|
|2fo           |            61.818905|                      4|       11532|            724.6260|              716.0000|         46|         16.83934|                 12|    1942|
|4long         |             5.000000|                      5|           4|                  NA|                    NA|         NA|               NA|                 NA|      NA|
|4to           |            43.762006|                     12|       16528|            412.8611|              439.0000|         27|         15.87355|                  8|   12187|
|8vo           |           143.595379|                     68|       11599|            406.7889|              413.3333|        181|         28.47034|                 28|    3810|
|12long        |            67.000000|                     50|          10|             24.0000|               24.0000|          1|         28.80000|                 24|       5|
|12mo          |           184.150964|                    162|        3021|            260.5657|              211.0000|         47|         26.26923|                 24|     520|
|16mo          |           163.645570|                    116|          81|                  NA|                    NA|         NA|         30.46154|                 24|      13|
|18mo          |           177.575758|                    158|          33|            172.0000|              172.0000|          1|         41.00000|                 41|       2|
|24long        |           244.000000|                    244|           1|                  NA|                    NA|         NA|               NA|                 NA|      NA|
|24mo          |           193.525000|                    181|          43|                  NA|                    NA|          2|         23.27273|                 24|      11|
|32mo          |           182.000000|                    193|           6|                  NA|                    NA|         NA|               NA|                 NA|      NA|
|48mo          |           128.000000|                    128|           1|                  NA|                    NA|         NA|               NA|                 NA|      NA|
|64mo          |           197.000000|                    197|           2|                  NA|                    NA|         NA|               NA|                 NA|      NA|
|NA            |            14.083557|                      2|        3003|                  NA|                    NA|         NA|         18.87593|                 15|     403|


![plot of chunk summarypagecountsmulti2](figure/summarypagecountsmulti2-1.png)


## Average document dimensions 


```
## Error: Unknown parameters: method
```

![plot of chunk summaryavedimstime](figure/summaryavedimstime-1.png)



|gatherings | mean.height| median.height| mean.width| median.width|     n|
|:----------|-----------:|-------------:|----------:|------------:|-----:|
|1to        |    59.97151|      59.97151|   89.95574|     89.95574|  3615|
|2fo        |    31.37762|      31.37762|   47.10090|     47.10090| 12171|
|4to        |    21.91628|      21.91628|   27.87294|     27.87294| 16543|
|8vo        |    13.01510|      13.01510|   19.02952|     19.02952| 11719|
|12mo       |    12.49440|      12.49440|   18.98666|     18.98666|  3035|
|16mo       |    12.00000|      12.00000|   15.00000|     15.00000|    81|
|18mo       |    10.00000|      10.00000|   16.00000|     16.00000|    33|
|24mo       |     8.50000|       8.50000|   12.50000|     12.50000|    45|
|NA         |    20.98898|      20.98898|   31.65239|     31.65239|   817|

## Histograms of all entries for numeric variables

![plot of chunk summary-histograms](figure/summary-histograms-1.png)![plot of chunk summary-histograms](figure/summary-histograms-2.png)![plot of chunk summary-histograms](figure/summary-histograms-3.png)![plot of chunk summary-histograms](figure/summary-histograms-4.png)![plot of chunk summary-histograms](figure/summary-histograms-5.png)![plot of chunk summary-histograms](figure/summary-histograms-6.png)![plot of chunk summary-histograms](figure/summary-histograms-7.png)![plot of chunk summary-histograms](figure/summary-histograms-8.png)![plot of chunk summary-histograms](figure/summary-histograms-9.png)![plot of chunk summary-histograms](figure/summary-histograms-10.png)![plot of chunk summary-histograms](figure/summary-histograms-11.png)![plot of chunk summary-histograms](figure/summary-histograms-12.png)![plot of chunk summary-histograms](figure/summary-histograms-13.png)

## Histograms of the top entries for factor variables

![plot of chunk summary-bars](figure/summary-bars-1.png)![plot of chunk summary-bars](figure/summary-bars-2.png)![plot of chunk summary-bars](figure/summary-bars-3.png)![plot of chunk summary-bars](figure/summary-bars-4.png)![plot of chunk summary-bars](figure/summary-bars-5.png)![plot of chunk summary-bars](figure/summary-bars-6.png)![plot of chunk summary-bars](figure/summary-bars-7.png)![plot of chunk summary-bars](figure/summary-bars-8.png)![plot of chunk summary-bars](figure/summary-bars-9.png)![plot of chunk summary-bars](figure/summary-bars-10.png)


<!--
### Testing rCharts example - perhaps only in HTML with knit2html
<iframe srcdoc=' &lt;!doctype HTML&gt;
&lt;meta charset = &#039;utf-8&#039;&gt;
&lt;html&gt;
  &lt;head&gt;
    
    &lt;link rel=&#039;stylesheet&#039; href=&#039;//cdnjs.cloudflare.com/ajax/libs/nvd3/1.1.15-beta/nv.d3.min.css&#039;&gt;
    
    
    
    &lt;script src=&#039;//ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    
    &lt;script src=&#039;//d3js.org/d3.v3.min.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    
    &lt;script src=&#039;//cdnjs.cloudflare.com/ajax/libs/nvd3/1.1.15-beta/nv.d3.min.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    
    &lt;script src=&#039;//nvd3.org/assets/lib/fisheye.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    
    
    &lt;style&gt;
    .rChart {
      display: block;
      margin-left: auto; 
      margin-right: auto;
      width: 800px;
      height: 400px;
    }  
    &lt;/style&gt;
    
  &lt;/head&gt;
  &lt;body &gt;
    
    &lt;div id = &#039;chart1a259ed4f5d&#039; class = &#039;rChart nvd3&#039;&gt;&lt;/div&gt;    
    &lt;script type=&#039;text/javascript&#039;&gt;
 $(document).ready(function(){
      drawchart1a259ed4f5d()
    });
    function drawchart1a259ed4f5d(){  
      var opts = {
 &quot;dom&quot;: &quot;chart1a259ed4f5d&quot;,
&quot;width&quot;:    800,
&quot;height&quot;:    400,
&quot;x&quot;: &quot;Hair&quot;,
&quot;y&quot;: &quot;Freq&quot;,
&quot;group&quot;: &quot;Eye&quot;,
&quot;type&quot;: &quot;multiBarChart&quot;,
&quot;id&quot;: &quot;chart1a259ed4f5d&quot; 
},
        data = [
 {
 &quot;Hair&quot;: &quot;Black&quot;,
&quot;Eye&quot;: &quot;Brown&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             32 
},
{
 &quot;Hair&quot;: &quot;Brown&quot;,
&quot;Eye&quot;: &quot;Brown&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             53 
},
{
 &quot;Hair&quot;: &quot;Red&quot;,
&quot;Eye&quot;: &quot;Brown&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             10 
},
{
 &quot;Hair&quot;: &quot;Blond&quot;,
&quot;Eye&quot;: &quot;Brown&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              3 
},
{
 &quot;Hair&quot;: &quot;Black&quot;,
&quot;Eye&quot;: &quot;Blue&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             11 
},
{
 &quot;Hair&quot;: &quot;Brown&quot;,
&quot;Eye&quot;: &quot;Blue&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             50 
},
{
 &quot;Hair&quot;: &quot;Red&quot;,
&quot;Eye&quot;: &quot;Blue&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             10 
},
{
 &quot;Hair&quot;: &quot;Blond&quot;,
&quot;Eye&quot;: &quot;Blue&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             30 
},
{
 &quot;Hair&quot;: &quot;Black&quot;,
&quot;Eye&quot;: &quot;Hazel&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             10 
},
{
 &quot;Hair&quot;: &quot;Brown&quot;,
&quot;Eye&quot;: &quot;Hazel&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             25 
},
{
 &quot;Hair&quot;: &quot;Red&quot;,
&quot;Eye&quot;: &quot;Hazel&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              7 
},
{
 &quot;Hair&quot;: &quot;Blond&quot;,
&quot;Eye&quot;: &quot;Hazel&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              5 
},
{
 &quot;Hair&quot;: &quot;Black&quot;,
&quot;Eye&quot;: &quot;Green&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              3 
},
{
 &quot;Hair&quot;: &quot;Brown&quot;,
&quot;Eye&quot;: &quot;Green&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:             15 
},
{
 &quot;Hair&quot;: &quot;Red&quot;,
&quot;Eye&quot;: &quot;Green&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              7 
},
{
 &quot;Hair&quot;: &quot;Blond&quot;,
&quot;Eye&quot;: &quot;Green&quot;,
&quot;Sex&quot;: &quot;Male&quot;,
&quot;Freq&quot;:              8 
} 
]
  
      if(!(opts.type===&quot;pieChart&quot; || opts.type===&quot;sparklinePlus&quot; || opts.type===&quot;bulletChart&quot;)) {
        var data = d3.nest()
          .key(function(d){
            //return opts.group === undefined ? &#039;main&#039; : d[opts.group]
            //instead of main would think a better default is opts.x
            return opts.group === undefined ? opts.y : d[opts.group];
          })
          .entries(data);
      }
      
      if (opts.disabled != undefined){
        data.map(function(d, i){
          d.disabled = opts.disabled[i]
        })
      }
      
      nv.addGraph(function() {
        var chart = nv.models[opts.type]()
          .width(opts.width)
          .height(opts.height)
          
        if (opts.type != &quot;bulletChart&quot;){
          chart
            .x(function(d) { return d[opts.x] })
            .y(function(d) { return d[opts.y] })
        }
          
         
        
          
        

        
        
        
      
       d3.select(&quot;#&quot; + opts.id)
        .append(&#039;svg&#039;)
        .datum(data)
        .transition().duration(500)
        .call(chart);

       nv.utils.windowResize(chart.update);
       return chart;
      });
    };
&lt;/script&gt;
    
    &lt;script&gt;&lt;/script&gt;    
  &lt;/body&gt;
&lt;/html&gt; ' scrolling='no' frameBorder='0' seamless class='rChart  nvd3  ' id='iframe-chart1a259ed4f5d'> </iframe>
 <style>iframe.rChart{ width: 100%; height: 400px;}</style>
-->

