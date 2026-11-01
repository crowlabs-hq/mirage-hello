# mirage-hello

Minimalist hello-world skeleton for MirageOS.

### Cloning
1. Use it as a template by clicking on the "_**Use this template**_" button.

2. By creating a repository with GitHub's `gh` CLI:

    ```shell
    gh repo create mirage-hello -p crowlabs-hq/mirage-hello --clone
    ```

3. By directly cloning this repository with:

    ```shell
    git clone git@github.com:crowlabs-hq/mirage-hello.git
    ```

### Building
Build the unikernel (for the Unix target):

> [!NOTE]
> Use `-t hvt` instead of `-t unix` on Linux for Solo5 unikernels.

```shell
mirage configure -t unix
make depends
dune build
```

Finally, you can run it with:

```shell
./dist/hello
```

Optionally (to delete generated files):

```shell
mirage clean
```
