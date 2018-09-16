react-devloos
```
npm install
npm run build:extension:chrome
shells->chrome->build->packed.zip
    更多工具-》扩展程序-》
```


switch
```
 每次只渲染一个 
 <Switch>
  <Route path="/about" component={About}/>
  <Route path="/topics" component={Topics}/>
  <Route exact path="/" component={Home}/>
</Switch> -->
```

match
```
    let thisUrl = this.props.match.url;
字符拼接
    {thisUrl + "/"}
    {`${thisUrl}/`}
```

自定义组件
```
const MenuLink = ({to,label,activeOnlyWhenExact}) => {
    return(
        <Route 
            path={to}
            exact
            children={({match}) => 
                <div>
                    {match?">":""}
                    <Link to={to}>{label}</Link>
                </div>
        }
        />
    )
}
```
