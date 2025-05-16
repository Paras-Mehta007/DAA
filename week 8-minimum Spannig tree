#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;

int find(int u, vector<int> &parent) {
    return u == parent[u] ? u : parent[u] = find(parent[u], parent);
}

bool unite(int u, int v, vector<int> &parent, vector<int> &rank) {
    u = find(u, parent);
    v = find(v, parent);
    if (u == v) return false;
    if (rank[u] < rank[v]) swap(u, v);
    parent[v] = u;
    if (rank[u] == rank[v]) rank[u]++;
    return true;
}

int main() {
    int V;
    cin >> V;
    vector<tuple<int, int, int>> edges;
    int w;
    for (int i = 0; i < V; ++i)
        for (int j = 0; j < V; ++j) {
            cin >> w;
            if (w && i < j) edges.push_back({w, i, j});
        }
    sort(edges.rbegin(), edges.rend());
    vector<int> parent(V), rank(V, 0);
    for (int i = 0; i < V; ++i) parent[i] = i;
    int total = 0;
    for (auto [w, u, v] : edges)
        if (unite(u, v, parent, rank)) total += w;
    cout << "Maximum Spanning Weight: " << total << "\n";
}
