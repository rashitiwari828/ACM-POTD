Problem Statement _ fing centre of star graph

code:
class Solution {
public:

    int findCenter(vector<vector<int>>& edges) {
        if (edges[0][0] == edges[1][0] || edges[0][0] == edges[1][1]) {
            return edges[0][0];
        }
        return edges[0][1];
    }
};
screenshot:
<img width="1532" height="905" alt="Screenshot 2026-04-14 232611" src="https://github.com/user-attachments/assets/94478aef-2d89-40f0-b8bc-e82e6265cf95" />
