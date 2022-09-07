# ABDUL RAHEEM SYED

## The Nelson-Atkins Museum of Art

The Nelson-Atkins Museum of Art is an **Art museum** in Kansas City, Missouri, known for its encyclopedic collection of art from nearly every continent and culture, and especially for its extensive collection of Asian art.



---

# Directions from MCI to  Nelson-Atkins Museum
1. catch a taxi and go to the LAX airport
    1. take a flight from california to kansas airport(mca)
    2. take all ur belongings and book a taxi to henderson which takes 10-15 min from airport
2. wait for the taxi to arive near the location
    1. Sit back and enjoy the lightning and mountain view 
    2. Listen the music 
3. Finally we have reached our location.!!


* Sight seeing places around museum:
 * Parks:
    * Worlds of fun
    * Penn Valley Park
    * The Concourse Park
    * Penguin park
* Near by city:
    * St.Louis
    * Springfield
    * jefferson City
    * st.joseph
    * Cable 


*[AboutMe.md](AboutMe.md)*

---

# 4 cities i  loved and i would love to suggest
I am going to create a table with  4 cities that I would love to recommend someone visit = Long Beach,Florida, Chicago , New York , dayton.

|name of the city |locations to visit | duration|
|---|---|---|
|Long Beach|Beaches|2 days|
|Florida|Wild life|1 day|
|New york|Time Square|20 hrs|
|Chicago|Downtown|6 hrs|

---
# Pithy Quote

> “Money is a tool, so I don't have to be.”
 *_Eddie Mumford*

<Br>
> "Hell is empty and all the devils are here." William Shakespeare


---

# Dijkstra Algorithm
> Dijkstra's algorithm is an algorithm for finding the shortest paths between nodes in a graph, which may represent, for example, road networks. It was conceived by computer scientist Edsger W. Dijkstra in 1956 and published three years later. The algorithm exists in many variant

[Click Here to Know More](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm)




const int INF = 1000000000;
vector<vector<pair<int, int>>> adj;

void dijkstra(int s, vector<int> & d, vector<int> & p) {
    int n = adj.size();
    d.assign(n, INF);
    p.assign(n, -1);
    vector<bool> u(n, false);

    d[s] = 0;
    for (int i = 0; i < n; i++) {
        int v = -1;
        for (int j = 0; j < n; j++) {
            if (!u[j] && (v == -1 || d[j] < d[v]))
                v = j;
        }

        if (d[v] == INF)
            break;

        u[v] = true;
        for (auto edge : adj[v]) {
            int to = edge.first;
            int len = edge.second;

            if (d[v] + len < d[to]) {
                d[to] = d[v] + len;
                p[to] = v;
            }
        }
    }
}

[code source](https://cp-algorithms.com/graph/dijkstra.html)