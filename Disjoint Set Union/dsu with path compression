ll a[MAX];
ll siz[MAX];
void st(ll n)
{
  for(ll i=0;i<=n;i++)
  {
    a[i]=i;
    siz[i]=1;
  }
}
int root(ll r)
{
    if(a[r]==r) 
      return r;
    else 
      return a[r]=root(a[r]);
}
void unionn(ll u,ll v)
{
    u=root(u);
    v=root(v);
    if(u==v)
      return ;
    if(siz[v]>siz[u])
        swap(v,u);
    a[v]=u;
    siz[u]+=siz[v];
}
