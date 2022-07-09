# template

## 解析lambda出入参类型

```cpp
template<typename T>
struct memfunc_type {
    using type = T;
};
template<typename Ret, typename Class, typename... Args>
struct memfunc_type<Ret(Class::*)(Args...)const> {
    using type = std::function<Ret(args...)>;
};
template<typename F>
typename memefunc_type<decltype(&F::operator())>::type lambda_type_parse(F const& func) {
    ...
}

template<typename... Args>
void function_parse(std::function<void(Args...)> f) {
    ...
}

template<typename F>
auto test(F&& f) -> typename memfunc_type<decltype(&F::operator())>::type {
    return memfunc_type<decltype(&F::operator())>::type(f);
}
```