EXACT
==== 
EXACT: Attributed Entity Extraction By Annotating Texts
----
<h4>
&emsp;Attributed entity is an entity defined by its structural attributes. Extracting attributed entities from textual documents is an important problem for a variety of big-data applications. We propose a system called EXACT for extracting attributed entities from textual documents by performing explorative annotation tasks, which create attributes and bind them to tag values. To support efficient annotation, we propose a novel tag recommendation technique based on a few-shot learning scheme which can predict tags for new annotation tasks given very few human-annotated samples. We also propose a document recommendation scheme to provide run-time context for the user. Using a novel attribute index, the system can generate the task-relevant attributed entities on-the-fly. We demonstrate how these techniques can be integrated behind a novel user interface to enable productive and efficient extraction of attributed entities at limited cost in human annotation.</h4>

System Design
----
![system design](https://github.com/yysys/EXACT/blob/master/images/system_design.png)

##EXACT contains four key components:
<h4>
1) The labelling module which iteratively runs interactive annotation tasks. These tasks display textual objects such as tags, document snippets, and attributes in a few crafted Web pages, and collect various feedback from the user. The feedback might be to create a new attribute, to confirm a recommended tag as a value for an attribute, to select a tag in a snippet as a synonym of a value, and so forth.
</h4>
<h4>
2) The attribute indexer which dynamically captures in the index all the necessary information produced from the labelling module. The indexed information includes the attributes, the values, and the information of documents linked to each value. Each time an annotation task is submitted, the indexer takes necessary steps to update the index. The subsequent annotation tasks would also take the latest changes in the indexed attributes/values into the loop.
</h4>
<h4>
3) The recommender module which generates recommended objects for the annotation pages using a number of recommendation algorithms based on heuristic rules and machine-learning models.
</h4>
<h4>
4) The entity generation module which generates AEs from the indexer. As generating all entities in a single batch is expensive in computation and not user-friendly, we choose to generate entities selectively in response to each finished annotation task. After each feedback, the new generated AEs can be displayed in the browser as a cue for further operations.
</h4>

##EXACT INPUT
![system design](https://github.com/yysys/EXACT/blob/master/images/exact_input.png)
##EXACT OUTPUT
![system design](https://github.com/yysys/EXACT/blob/master/images/exact_output.png)
##EXACT USR INTERFACE
![system design](https://github.com/yysys/EXACT/blob/master/images/user%20interface.png)

