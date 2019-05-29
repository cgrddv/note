### 持久化缓存方案
  vuex-persistedstate
  同一chrome，不同tab，想要登录不同的用户
  session+local
  ~~~
  createPersistedState({
            storage: {
                getItem: key => {
                    return sessionStorage.getItem(key) || localStorage.getItem(key)
                },
                setItem: (key, value) => {
                    sessionStorage.setItem(key, value)
                    localStorage.setItem(key, value)
                },
                removeItem: key => {
                    sessionStorage.removeItem(key)
                    localStorage.removeItem(key)
                }
            }
        })
  ~~~
