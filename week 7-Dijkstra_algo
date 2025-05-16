#include <iostream>
#include <vector>
#include <queue>
using namespace std;

int main() {
    int V;
    cin >> V;
    vector<vector<pair<int, int>>> adj(V);
    int weight;
    for (int i = 0; i < V; ++i)
        for (int j = 0; j < V; ++j) {
            cin >> weight;
            if (weight) adj[i].push_back({j, weight});
        }
    int src;
    cin >> src;
    vector<int> dist(V, 1e9), parent(V, -1);
    dist[src] = 0;
    priority_queue<pair<int, int>, vector<pair<int, int>>, greater<>> pq;
    pq.push({0, src});
    while (!pq.empty()) {
        auto [d, u] = pq.top(); pq.pop();
        for (auto [v, w] : adj[u]) {
            if (dist[u] + w < dist[v]) {
                dist[v] = dist[u] + w;
                parent[v] = u;
                pq.push({dist[v], v});
            }
        }
    }
    for (int i = 0; i < V; ++i) {
        cout << i << ":";
        vector<int> path;
        for (int x = i; x != -1; x = parent[x])
            path.push_back(x);
        for (int j = path.size() - 1; j >= 0; --j)
            cout << path[j] << (j ? "->" : "");
        cout << " " << dist[i] << "\n";
    }
}
