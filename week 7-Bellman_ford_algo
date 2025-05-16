#include <iostream>
#include <vector>
using namespace std;

int main() {
    int V;
    cin >> V;
    vector<vector<int>> mat(V, vector<int>(V));
    vector<tuple<int, int, int>> edges;
    for (int i = 0; i < V; ++i)
        for (int j = 0; j < V; ++j) {
            cin >> mat[i][j];
            if (mat[i][j] != 0) edges.push_back({i, j, mat[i][j]});
        }
    int src;
    cin >> src;
    vector<int> dist(V, 1e9), parent(V, -1);
    dist[src] = 0;
    for (int i = 0; i < V - 1; ++i)
        for (auto [u, v, w] : edges)
            if (dist[u] + w < dist[v]) {
                dist[v] = dist[u] + w;
                parent[v] = u;
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
