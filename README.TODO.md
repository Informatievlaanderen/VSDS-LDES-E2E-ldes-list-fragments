# TODO
* (allow to follow any node: LDES, view, structure node or data node)
* follow view only
* (by default) only check structure
* (allow to follow data nodes as well)
* request (start) node:
  * 200: continue
  * 302: follow location header
  * 4xx/5xx: log error
  * other: log warning
* check start node type
  * LDES: check available view count
    * N > 1: error, need to select a view
    * N = 0: error, cannot follow LDES
    * N = 1: follow view instead
  * view: follow view
  * structure: follow structure
  * data node: error if not following data nodes
* log node retrieved
* follow node: same as now, but if following only structure, check if data node and ignore if so
