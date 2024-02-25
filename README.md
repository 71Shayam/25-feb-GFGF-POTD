long long int count(long long int n)
    {
    	// Your code here
    	vector<long long>ans(n+1, 0);
    	ans[0]=1;
    	for(int i=3;i<=n;i++){
    	    ans[i]+=ans[i-3];
    	}
    	for(int i=5;i<=n;i++){
    	    ans[i]+=ans[i-5];
    	}
    	for(int i=10;i<=n;i++){
    	    ans[i]+=ans[i-10];
    	}
    	
    	return ans[n];
    	
    }
