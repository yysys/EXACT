EXACT
==== 
EXACT: Attributed Entity Extraction By Annotating Texts
    Attributed entity is an entity defined by its structural attributes.
Extracting attributed entities from textual documents is an important problem for a variety of big-data applications. We propose a
system called EXACT for extracting attributed entities from textual documents by performing explorative annotation tasks, which
create attributes and bind them to tag values. To support efficient
annotation, we propose a novel tag recommendation technique
based on a few-shot learning scheme which can predict tags for
new annotation tasks given very few human-annotated samples.
We also propose a document recommendation scheme to provide
run-time context for the user. Using a novel attribute index, the
system can generate the task-relevant attributed entities on-the-fly.
We demonstrate how these techniques can be integrated behind a
novel user interface to enable productive and efficient extraction of
attributed entities at limited cost in human annotation.

System Design
----
![system design](https://github.com/yysys/EXACT/blob/master/images/system_design.png)



