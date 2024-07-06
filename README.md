Topological sorting for Directed Acyclic Graph (DAG) is a linear ordering of vertices such 
that for every directed edge u-v, vertex u comes before v in the ordering.



#topological sort
vector<int> topoSort(int V, vector<int> adj[]) {
    vector<int> indegree(V, 0);
    // Calculate indegree of each vertex
    for (int i = 0; i < V; i++) {
        for (auto j : adj[i]) {
            indegree[j]++;
        }
    }
    queue<int> q;
    for (int i = 0; i < V; i++) {
        if (indegree[i] == 0)
            q.push(i);
    }
    vector<int> ans;
    while (!q.empty()) {
        int front = q.front();
        q.pop();
        ans.push_back(front);
        for (auto ele : adj[front]) {
            indegree[ele]--;
            if (indegree[ele] == 0)
                q.push(ele);
        }
    }
    return ans;
}

int main() {
    int V = 6;
    vector<int> adj[V];
    adj[5].push_back(2);
    adj[5].push_back(0);
    adj[4].push_back(0);
    adj[4].push_back(1);
    adj[2].push_back(3);
    adj[3].push_back(1);
    vector<int> result = topoSort(V, adj);
    cout << "Topological Sort: ";
    for (int i : result) {
        cout << i << " ";
    }
    cout << endl;
    return 0;
}
