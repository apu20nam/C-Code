# C-Code
This c++ Code is Maximum Ice Cream Bars
 int maxIceCream(vector<int>& costs, int coins) {
        sort(costs.begin(),costs.end());
        int n=costs.size();
        if(costs[0]>coins)return 0;
        int maxIceCream=0;
        for(int i=0;i<n;i++)
        {
            if(costs[i]<=coins)
            {
               coins=coins-costs[i];
               maxIceCream= maxIceCream+1;
            }
            else
            {
                return maxIceCream;
            }
        }
        return maxIceCream;
    }
