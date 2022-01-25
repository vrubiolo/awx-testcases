# awx-testcases
Various public testcases for AWX


No extra variables specified, Jinja template will remain unevaluated
```bash
./run

TASK [vars-eval : print variables values] *****************************************************************************
ok: [test_host] => {
    "msg": "vincent_inv_var_simple: foo, vincent_inv_var_jinja: {{ jinja_variable_value }}"
}
```

Extra variable specified, this will evaluate the Jinja expression. Can also be
done using `./run -e @./extra_vars`
```bash
./run_extra_vars

TASK [vars-eval : print variables values] *****************************************************************************
ok: [test_host] => {
    "msg": "vincent_inv_var_simple: foo, vincent_inv_var_jinja: jinja_bar"
}
```
