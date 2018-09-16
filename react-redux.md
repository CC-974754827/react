.js
```
<Provider store={store}></Provider>
```
store
保存数据
```
import {createStore} from 'redux';

const initialState = 0;
const store = createStore(()=>{},initialState);
export default store;
```
action
在.js中
```
const add=()=>{
    return{
        type:'ADD'
    }
}
```
reducer
接收旧的state和action
```
import {combineReducers} from 'redux';
const count = (state=0,action)=>{
    switch(action.type){
        case:'ADD':
        return state+1;
        default:
        return state;
    }
}
const reducer = combineReducers({
    count
})
export default reducer;
```
connect
获取state
```
const mapStateToProps=(state)=>({
    count:state.count
})

const mapDispatchToProps = (dispatch) =>{
    return{
        add:()=>dispatch(add())
    };
}
```
