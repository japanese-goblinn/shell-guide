# shell guide by japanese-goblinn

## Variables

```shell
GLOBAL_VAR="1"
local_var="hello"

# prefer $VAR over ${VAR}
echo "$local_var"

# use ${VAR} to separate variables from text
echo "$local_varsome text" # 🛑 mistake
echo "${local_vars}some text" # ✅ works as excpected

# use ${VAR} to impove readablility 
echo "$GLOBAL_VAR$local_var" # works, but not readable
echo "${GLOBAL_VAR}$local_var" # better

# always wrap variables in `""` to prevent unexpected globbing
# drop `""` only if globbing behaviour is what you need
# TODO: example
```

## Resources

- [koalaman/shellcheck: ShellCheck, a static analysis tool for shell scripts](https://github.com/koalaman/shellcheck)
	- useful set of rules
