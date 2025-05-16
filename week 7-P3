#include <iostream>
#include <vector>
using namespace std;

int main() {
    int V;
    cin >> V;
    vector<vector<int>> graph(V, vector<int>(V));
    for (int i = 0; i < V; ++i)
        for (int j = 0; j < V; ++j)
            cin >> graph[i][j];
    int u, v, k;
    cin >> u >> v >> k;
    vector<vector<vector<int>>> dp(V, vector<vector<int>>(V, vector<int>(k + 1, 1e9)));
    for (int e = 0; e <= k; ++e)
        for (int i = 0; i < V; ++i)
            for (int j = 0; j < V; ++j)
                if (e == 0 && i == j)
                    dp[i][j][e] = 0;
                else if (e > 0)
                    for (int a = 0; a < V; ++a)
                        if (graph[i][a])
                            dp[i][j][e] = min(dp[i][j][e], graph[i][a] + dp[a][j][e - 1]);
    if (dp[u][v][k] == 1e9) cout << -1 << "\n";
    else cout << dp[u][v][k] << "\n";
}
