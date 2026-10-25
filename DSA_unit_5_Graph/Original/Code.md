#include <iostream>
#include <vector>
#include <queue>
using namespace std;

void BFS(vector<vector<int>>& graph, int start)
{
    int n = graph.size();

    vector<bool> visited(n, false);
    queue<int> q;

    visited[start] = true;
    q.push(start);

    int count = 0;

    cout << "\nBFS Traversal Order: ";

    while (!q.empty())
    {
        int current = q.front();
        q.pop();

        cout << current << " ";
        count++;

        for (int neighbour : graph[current])
        {
            if (!visited[neighbour])
            {
                visited[neighbour] = true;
                q.push(neighbour);
            }
        }
    }

    cout << "\nNumber of reachable stops: "
         << count << endl;
}

int main()
{
    int n, e;

    cout << "Enter number of bus stops: ";
    cin >> n;

    if (n <= 0)
    {
        cout << "Invalid number of bus stops.";
        return 0;
    }

    vector<vector<int>> graph(n);

    cout << "Enter number of direct bus routes: ";
    cin >> e;

    if (e < 0)
    {
        cout << "Invalid number of bus routes.";
        return 0;
    }

    cout << "Enter routes (stop1 stop2):\n";

    for (int i = 0; i < e; i++)
    {
        int u, v;
        cin >> u >> v;

        if (u < 0 || u >= n ||
            v < 0 || v >= n)
        {
            cout << "Invalid bus stop number.";
            return 0;
        }

        graph[u].push_back(v);
    }

    int start;

    cout << "Enter starting bus stop: ";
    cin >> start;

    if (start < 0 || start >= n)
    {
        cout << "Invalid starting bus stop.";
        return 0;
    }

    BFS(graph, start);

    return 0;
}
