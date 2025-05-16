#include <iostream>
#include <vector>
#include <queue>
using namespace std;

int main() {
    int V;
    cin >> V;
    vector<vector<int>> graph(V, vector<int>(V));
    for (int i = 0; i < V; ++i)
        for (int j = 0; j < V; ++j)
            cin >> graph[i][j];
    vector<int> key(V, 1e9), inMST(V, false);
    key[0] = 0;
    int total = 0;
    for (int i = 0; i < V; ++i) {
        int u = -1;
        for (int j = 0; j < V; ++j)
            if (!inMST[j] && (u == -1 || key[j] < key[u]))
                u = j;
        inMST[u] = true;
        total += key[u];
        for (int v = 0; v < V; ++v)
            if (graph[u][v] && !inMST[v] && graph[u][v] < key[v])
                key[v] = graph[u][v];
    }
    cout << "Minimum Spanning Weight: " << total << "\n";
}
