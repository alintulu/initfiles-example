# initfiles-example

```
$ reana-client run -w initfiles-test -f reana-yadage.yaml
```

```
$ kubectl logs reana-run-batch-.... workflow-engine | less
$ /initfiles
```

You should see the files specified in reana.yaml there, something like 

```
'initfiles': ['/var/reana/users/00000000-0000-0000-0000-000000000000/workflows/bf7d5d5c-24b9-48a3-bdcf-2b488f5bbde0/workflow/yadage/first.yml', '/var/reana/users/00000000-0000-0000-0000-000000000000/workflows/bf7d5d5c-24b9-48a3-bdcf-2b488f5bbde0/workflow/yadage/second.yml']
```

```
$ kubectl logs reana-run-batch-.... workflow-engine | less
$ /initdata
```

You should see the content of the initfiles there. In this case you should see something like 

```
'initdata': {'first': ['test'], 'second': 'test2'}
```
