# initfiles-example

```
$ reana-client run -w initfiles-test -f reana-yadage.yaml
```

```
$ kubectl logs reana-run-batch-.... workflow-engine | less
$ :/initfiles
```

You should see the files specified in reana.yaml there, something like `initfiles: [first.yml, second.yml]`

```
$ kubectl logs reana-run-batch-.... workflow-engine | less
$ :/initdata
```

You should see the content of the initfiles there. In this case you should see something like `ìnitdata: {first: [test], second: "test", ...}`
