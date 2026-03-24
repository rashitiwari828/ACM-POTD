  Problem Statement - Best time to buy and sell stock
  
  You are given an array prices where prices[i] is the price of a given stock on the ith day.
  You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock.
  Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return 0.

  code- 
  
  class Solution {
public:

    int maxProfit(vector<int>& prices) {
        int n= prices.size();
        int minPrice = INT_MAX;
        int maxProfit = 0;

        for(int i=0;i<n;i++){
            if(prices[i]<minPrice){
                minPrice=prices[i];
            }
            int Profit = prices[i]-minPrice;
            if(Profit > maxProfit){
                maxProfit=Profit;
            }
        
        }return maxProfit;
    }
};

ScreenShot- 
<img width="1883" height="842" alt="Screenshot 2026-03-24 184839" src="https://github.com/user-attachments/assets/dfefedbc-e442-4a96-94eb-91b8cad2b3e3" />

