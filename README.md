# Exploring Crossfilter

[Crossfilter](http://square.github.com/crossfilter/) provides fast n-dimensional filtering and grouping of records, enabling live histograms.  It's designed for exploring large multivariate datasets, where interactions consist of grouping by a dimension followed by incremental filtering and reducing along another dimension.

Have a look at the ...

* [Intro](http://square.github.io/crossfilter/)
* [API](https://github.com/square/crossfilter/wiki/API-Reference)
* [Tests](https://github.com/square/crossfilter/blob/master/test/crossfilter-test.js)


## Status

So far we've [worked through](tutorial/index.coffee.md) [this tutorial](http://eng.wealthfront.com/2012/09/explore-your-multivariate-data-with-crossfilter.html) and demonstrated how to [filter by regex](examples/regex-filter.coffee.md).

We should incorporate select examples from the [tests](https://github.com/square/crossfilter/blob/master/test/crossfilter-test.js) as well as a few [custom filters](https://github.com/square/crossfilter/pull/36).

In particular, we should provide an example of [multi-value filtering](https://github.com/square/crossfilter/pull/36#issuecomment-14782016).


## Related

Note that there's a dimensional charting library based on D3 and Crossfilter
called [dc.js](http://nickqizhu.github.io/dc.js/). Looks convenient if
you're working on a web-based dashboard and cool with the predefined chart types.

If you need to construct aggregations with crossfilter, see the [reductio](http://esjewett.com/blog/reductio) library.  It helps build up aggregation functions that work correctly and efficiently with crossfilter's model.

If you're dealing with categorical data (e.g., surveys), try [catcorr.js](https://github.com/deanmalmgren/catcorrjs).

If you're dealing with streaming time series, see [cube.js](https://github.com/square/cube).

For inspiration on how crossfilter might be used in conjunction with a nicely structured query interface for a particular domain, check out the [Harvest](http://harvest.research.chop.edu/) [demo](http://harvest.research.chop.edu/demo/query/) and read the [manifesto](http://harvest.research.chop.edu/manifesto/).  Similarly, crossfilter enables interactive exploration of spatio-temporal data in Stanford's [Palladio](http://esjewett.com/blog/palladio) project for the digital humanities.
