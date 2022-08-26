# Deploying Aleo Programs in Testnet3

This guide is a walkthrough on how to deploy Aleo programs in Testnet3 using the Aleo SDK.

Before you can start deploying Aleo programs you must have the Aleo SDK installed and must have an Aleo Program created.

You can follow the steps detailed in [our previous post](https://www.entropy1729.com/aleo-development-starter-pack/).

## Deploying our Aleo project

To deploy a program we first need to have a program to deploy:

```bash
aleo new foo
```

After creating your program, you can deploy it with:

```bash
cd foo

aleo deploy
```

When you have done this you should see the following output:

```bash
⏳ Deploying 'foo.aleo'...

 • Loaded universal setup (in 2174 ms)
 • Built 'hello' (in 12970 ms)
 • Certified 'hello': 657 ms

✅ Deployed 'foo.aleo' (in "[...]/foo")
```

If you run `aleo deploy` outside your program directory (let's say inside `/not_foo`) the latter is not going to be deployed and the console output should log:

```bash
⚠️  Missing 'program.json' at '[...]/not_foo'
```

And that is how you deploy an Aleo project. Easy right? That's the idea 😉.

## Working with Aleo Programs in Testnet3

During Testnet3's life cycle all program deployments will be expenditure to the blockchain by Aleo Explorer on behalf of the user so no user credit spent is needed!

This will help to get useful metrics and speed up the development of this testnet! 
