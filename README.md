# return-task
In c# return a task
```
public async Task<return type> MethodA()
        {
            return Task.FromResult<return type>(
                ((Func<return type>)(() =>
            {
                // return your code;
            }))());
        }

```

## Example -
```

public async Task<Dictionary<uint, UserSecuritySetting>> GetUserSecuritySettings()
        {
            return Task.FromResult<Dictionary<uint, UserSecuritySetting>>(
                ((Func<Dictionary<uint, UserSecuritySetting>>)(() =>
            {
                return UserSecurityDto.GetList();
            }))());
        }

```
