Problem Statement - Flood Fill

code:
class Solution {
public:

    void dfs(vector<vector<int>>& image, int r, int c, int oldColor, int newColor) {
    
        if (r < 0 || c < 0 || r >= image.size() || c >= image[0].size()) return;

        
        if (image[r][c] != oldColor) return;

        
        image[r][c] = newColor;

        dfs(image, r+1, c, oldColor, newColor);
        dfs(image, r-1, c, oldColor, newColor);
        dfs(image, r, c+1, oldColor, newColor);
        dfs(image, r, c-1, oldColor, newColor);
    }

    vector<vector<int>> floodFill(vector<vector<int>>& image, int sr, int sc, int newColor) {
        int oldColor = image[sr][sc];
        if (oldColor != newColor) {   
            dfs(image, sr, sc, oldColor, newColor);
        }
        return image;
       
    }
};

Screenshot:
<img width="1792" height="817" alt="Screenshot 2026-04-12 224011" src="https://github.com/user-attachments/assets/8dbfd728-20fe-49cd-8a9a-9701600484b0" />
