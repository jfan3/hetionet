# Hetionet: an integrative network of disease

Hetionet is a hetnet — network with multiple node and edge (relationship) types — which encodes biology. The hetnet was designed for [Project Rephetio](https://doi.org/10.15363/thinklab.4 "Repurposing drugs on a hetnet · Project Rephetio on Thinklab"), which aims to systematically identify why drugs work and predict new therapies for drugs.
The research article describing Project Rephetio and Hetionet v1.0 is:

> [**Systematic integration of biomedical knowledge prioritizes drugs for repurposing**](https://doi.org/10.7554/eLife.26726)<br>
<small>Daniel S Himmelstein, Antoine Lizee, Christine Hessler, Leo Brueggeman, Sabrina L Chen, Dexter Hadley, Ari Green, Pouya Khankhanian, Sergio E Baranzini</small><br>
_eLife_ (2017-09-22) DOI: `10.7554/eLife.26726`

Version 1.0 contains 47,031 nodes of 11 types and 2,250,197 relationships of 24 types. This repository is currently only a download location for Hetionet. The data integration and hetnet creation occurs in a separate repository ([`dhimmel/integrate`](https://github.com/dhimmel/integrate/tree/d482033bcaa913a976faf4a6ee08497281c739c3)) and is imported to this repository by [`import.ipynb`](import.ipynb).

## Download Hetionet

[![Latest Zenodo DOI](https://zenodo.org/badge/56091268.svg)](https://zenodo.org/badge/latestdoi/56091268)

The network is available in three formats:

+ **JSON** — see [`hetnet/json`](hetnet/json)
+ **Neo4j** — see [`hetnet/neo4j`](hetnet/neo4j)
+ **TSV** — see [`hetnet/tsv`](hetnet/tsv)

The JSON and Neo4j formats contain node and edge properties, which are missing from the TSVs, including licensing information. Therefore the recommended formats are JSON and Neo4j. Our [`hetio` package](https://github.com/dhimmel/hetio "Hetnets in Python · GitHub") in Python reads the JSON format, but it is otherwise a simple yet new format. The Neo4j graph database has an established and thriving ecosystem. However, if you would like to access Hetionet without Neo4j, then we suggest the JSON format. Additional usage information is available at the corresponding download locations.

### Permuted Hetnets

We've created five permuted derivatives of Hetionet. The [permutation](https://doi.org/10.15363/thinklab.d136 "Permuting hetnets and implementing randomized edge swaps in cypher · Thinklab discussion") randomizes edges while preserving node degree. Permuted hetnets are available in [`hetnet/permuted`](hetnet/permuted) in JSON and Neo4j 2.3 formats. Relationship properties are omitted from the permuted hetnets.

## Network Description

[`describe`](describe) contains summary statistics on the hetnet. See [`describe/nodes/metanodes.tsv`](describe/nodes/metanodes.tsv) for details on the node types in the hetnet. See [`describe/edges/metaedges.tsv`](describe/edges/metaedges.tsv) for details on the edge types.

Below, we provide two hetnet visualizations. Panel A shows the metagraph (graph of types) for Hetionet. Panel B shows the actual hetnet with nodes laid out in circles by type. Color denotes edge type.

![Hetionet v1.0 visualizations](https://github.com/dhimmel/rephetio/blob/103054a2bc3f86998fed6cb3753d1ecdb5cbe1e7/figure/hetionet-v1.0-metagraph-and-graph.png?raw=true "A) Metagraph B) Hetionet in circular metanode layout")

## License

All original content in this repository is released as [CC0](https://creativecommons.org/publicdomain/zero/1.0/ "CC0 1.0 Universal · Public Domain Dedication"). However, the hetnet integrates data from many resources and users should consider the licensing of each source (see [this table](https://github.com/dhimmel/integrate/blob/d482033bcaa913a976faf4a6ee08497281c739c3/licenses/README.md "Source license table")). We apply a `license` attribute on a per node and per edge basis for sources with defined licenses. However, some resources don't provide any license, so for those we've requested permission. More information is [available on Thinklab](https://thinklab.com/discussion/integrating-resources-with-disparate-licensing-into-an-open-network/107 "Integrating resources with disparate licensing into an open network").
# drug_project
