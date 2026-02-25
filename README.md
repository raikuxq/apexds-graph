# @apexds/graph
A comprehensive TypeScript library for graph data structures (directed, undirected) and advanced graph algorithms (BFS, DFS, Dijkstra, transpose, has path, shortest path.).

[![npm version](https://img.shields.io/npm/v/@apexds/graph.svg)](https://www.npmjs.com/package/@apexds/graph)
[![minzip](https://deno.bundlejs.com/badge?q=@apexds/graph)](https://bundlejs.com/?q=%40apexds%2Fgraph)


---

## Documentation

Detailed documentation is available at:  
[https://raikuxq-algorithms.netlify.app/guide/data-structures/graphs](https://raikuxq-algorithms.netlify.app/guide/data-structures/graph.html)

---

# Installing
Install by using any of these commands:
+ `yarn add @apexds/graph`
+ `npm install @apexds/graph --save`

## Core lib
Core (implementation, tests, docs): [@raikuxq/lab-ts-algorithms](https://github.com/raikuxq/lab-ts-algorithms/)

# Examples

```ts
import { 
  UndirectedGraph,
  shortestPath,
  EnumGraphTraversalType
} from '@apexds/graph';

const graph = new UndirectedGraph<string>();

graph
  .addVertex('London')
  .addVertex('Paris')
  .addVertex('Berlin')
  .addVertex('Tokyo');

graph
  .addEdge('London', 'Paris', 100)
  .addEdge('Paris', 'Berlin', 150)
  .addEdge('Berlin', 'Tokyo', 800)
  .addEdge('London', 'Berlin', 400);

const path = shortestPath({
  graph,
  from: 'London',
  to: 'Tokyo',
  traversalType: EnumGraphTraversalType.DIJKSTRA
});
```
