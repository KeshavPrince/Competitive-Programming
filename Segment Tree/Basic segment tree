ll seg[500005],v[500005];

void build(ll idx,ll s,ll e)
{
    if(s==e)
      seg[idx]=v[s];
    else
    {
      ll m=(s+e)>>1;
      build(2*idx+1,s,m);
      build(2*idx+2,m+1,e);
      seg[idx]=seg[2*idx+1]+seg[2*idx+2];
    }
}

void modify(ll idx,ll x,ll val,ll s,ll e)
{
  if(s>e or x>e or x<s)
    return ;
  if(s==e)
    seg[idx]+=val;
  else
  {
    ll m=(s+e)>>1;
    modify(2*idx+1,x,val,s,m);
    modify(2*idx+2,x,val,m+1,e);
    seg[idx]=seg[2*idx+1]+seg[2*idx+2];
  }
}

ll query(ll idx,ll s,ll e,ll x,ll y)
{
  if(s>y or e<x)
    return 0;
  if(s>=x and e<=y)
    return seg[idx];
  else
  {
    ll m=(s+e)>>1;
    ll a=query(2*idx+1,s,m,x,y);
    ll b=query(2*idx+2,m+1,e,x,y);
    return a+b;
  }
}
