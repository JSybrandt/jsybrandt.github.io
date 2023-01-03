+++
title = "Partition Hypergraphs with Embeddings (Supplemental Info.)"
date = "2019-07-21T00:14:35-04:00"
draft = false
aliases = [
  "/2019/supl/partition/",
]
+++

[Go back to publication.][paper_link]

# Data

Download our full results as a [MongoDB Database dump][mongo_dump].
Explore these results within MongoDB with the `mongorestore` command.
More information can be found [here][mongo_restore_tut].

# Data Visualization

Select the desired comparison using the following buttons.
Then, click a cell in the resulting matrix plot to view a graph-wise
comparison.


<!-- The following is the visualization... -->

<style>
#matrix_content {
}

.large_img {
	zoom:.25;
}

.btn-group {
  margin:auto;
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin-bottom: 10pt;
}

.btn-group button {
  background-color: #4CAF50; /* Green background */
  border: 1px solid green; /* Green border */
  color: white; /* White text */
  padding: 10px 24px; /* Some padding */
  cursor: pointer; /* Pointer/hand icon */
  float: left; /* Float the buttons side by side */
}

/* Clear floats (clearfix hack) */
.btn-group:after {
  content: "";
  clear: both;
  display: table;
}

.btn-group button:not(:last-child) {
  border-right: none; /* Prevent double borders */
}

/* Add a background color on hover */
.btn-group button:hover {
  background-color: #3e8e41;
}
</style>

<div class="btn-group" id="partition_metric_button_group">
  <button class="part" id="km1_button" data="km1">Lambda - 1</button>
  <button class="part" id="cut_button" data="cut"># Cut Hyperedges</button>
</div>
<div class="btn-group" id="improvement_metric_button_group">
  <button class='imp' id="avg_button" data="avg">Average</button>
  <button class='imp' id="std_button" data="std">Standard Deviation</button>
  <button class='imp' id="min_button" data="min">Minimum Seen</button>
  <button class='imp' id="max_button" data="max">Maximum</button>
</div>
<div id=matrix_content>
</div>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
<script>

  current_part_met_str = "km1"
  current_imp_met_str = "avg"

  function set_content(partition_metric_str, improvement_metric_str){
    origin = "/img/data/partition_hypergraphs_with_embeddings/"
    file_path = "matrix_"
              + partition_metric_str
              + "_"
              + improvement_metric_str
              + ".html";
    $("#matrix_content").load(origin+file_path);
  }

  var buttons = document.getElementsByTagName("button");
  for(idx=0; idx < buttons.length; idx++){
    buttons[idx].onclick = function(){
      if(this.className === "part")
        current_part_met_str = this.getAttribute("data")
      if(this.className === "imp")
        current_imp_met_str = this.getAttribute("data")
      set_content(current_part_met_str, current_imp_met_str)
    }
  }
  set_content(current_part_met_str, current_imp_met_str);
	
</script>

# Hypergraph Data

The following depicts various properties per considered hypergraph.
For more explicit details per-graph, [we supply a detailed
table][hypergraph_detail_table].

![hypergraph data][hypergraph_data_img]



[paper_link]:/2019/partition
[mongo_dump]:https://drive.google.com/file/d/13ZRMFf0_VULYqoQHabgejJlsv-MEgn95/view?usp=sharing
[mongo_restore_tut]:https://docs.mongodb.com/manual/reference/program/mongorestore/#bin.mongorestore
[hypergraph_data_img]:/img/data/partition_hypergraphs_with_embeddings/hypergraph_data.png
[hypergraph_detail_table]:/misc/partition_with_embeddings_supl_hg_table/
