
#include <iostream>
#include <vector>
using namespace std;

bool dfs(int u, vector<vector<int>> &adj, vector<int> &visited) {
    visited[u] = 1;
    for (int v : adj[u]) {
        if (visited[v] == 1) return true;
        if (visited[v] == 0 && dfs(v, adj, visited)) return true;
    }
    visited[u] = 2;
    return false;
}

int main() {
    int V, E, u, v;
    cin >> V >> E;
    vector<vector<int>> adj(V);
    for (int i = 0; i < E; ++i) {
        cin >> u >> v;
        adj[u].push_back(v);
    }
    vector<int> visited(V, 0);
    bool hasCycle = false;
    for (int i = 0; i < V; ++i) {
        if (visited[i] == 0 && dfs(i, adj, visited)) {
            hasCycle = true;
            break;
        }
    }
    if (hasCycle) cout << "Yes Cycle Exists\n";
    else cout << "No Cycle Exists\n";
}
