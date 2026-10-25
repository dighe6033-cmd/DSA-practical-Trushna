#include <iostream>
#include <vector>
#include <queue>
using namespace std;

void BFS(vector<vector<int> >& graph, int start)
{
    int n = graph.size();

    vector<bool> visited(n, false);
    vector<int> level(n, -1);
    queue<int> q;

    visited[start] = true;
    level[start] = 0;
    q.push(start);

    int count = 0;

    cout << "\nBFS Traversal Order: ";

    while (!q.empty())
    {
        int current = q.front();
        q.pop();

        cout << current << " ";
        count++;

        for (int i = 0; i < graph[current].size(); i++)
{
    int neighbour = graph[current][i];

    if (!visited[neighbour])
    {
        visited[neighbour] = true;
        level[neighbour] = level[current] + 1;
        q.push(neighbour);
    

            }
        }
    }

    cout << "\n\nReachable Vertices and BFS Levels:\n";

    for (int i = 0; i < n; i++)
    {
        if (visited[i])
        {
            cout << "Vertex " << i
                 << " : Level " << level[i] << endl;
        }
    }

    cout << "\nNumber of reachable vertices: "
         << count << endl;

    cout << "Unvisited Vertices: ";

    bool found = false;

    for (int i = 0; i < n; i++)
    {
        if (!visited[i])
        {
            cout << i << " ";
            found = true;
        }
    }

    if (!found)
        cout << "None";

    cout << endl;
}

int main()
{
    int n, e;

    cout << "Enter number of vertices: ";
    cin >> n;

    if (n <= 0)
    {
        cout << "Invalid number of vertices.";
        return 0;
    }

    vector<vector<int> > graph(n);

    cout << "Enter number of edges: ";
    cin >> e;

    if (e < 0)
    {
        cout << "Invalid number of edges.";
        return 0;
    }

    cout << "Enter edges (u v):\n";

    for (int i = 0; i < e; i++)
    {
        int u, v;
        cin >> u >> v;

        if (u < 0 || u >= n ||
            v < 0 || v >= n)
        {
            cout << "Invalid vertex number.";
            return 0;
        }

        graph[u].push_back(v);
        graph[v].push_back(u);
    }

    int start;

    cout << "Enter starting vertex: ";
    cin >> start;

    if (start < 0 || start >= n)
    {
        cout << "Invalid starting vertex.";
        return 0;
    }

    BFS(graph, start);

    return 0;
}
