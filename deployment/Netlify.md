# Netlify

This is a guide on how you can deploy your App into Netlify.

1. Install Netlify CLI globally

```shell
  npm i -g netlify-cli
```

2. Login to your Netlify Account (Accept all)

```shell
 ntl login
```

3. Create a netlify.toml in the root directory

```shell
[build]
  publish = "public"
  functions = "functions"

[dev]
  autoLaunch = false
```

4. Run the command ntl init

```shell
ntl init
```

5. After following the instruction from init you can open your webpage

```shell
ntl open:site
||
ntl open:admin
```

# Sitenote

## Normal CRA Websites

```shell
ntl deploy
```

If the draft url looks good for you, you can then run

```shell
ntl deploy --prod
```

This will generate you a **production ready url**

## Serverless Functions

You can access your serverless function via the url `/.netlify/functions/name_of_the_function` in my case it would be `/.netlify/functions/hello-world`

## Publishing env to netlify

ENV is just locally avaible but with this method you can import it to the server and the developer in your team can use without creating a local file called .env its all in the netlify dashboard.

```shell
ntl env:import .env

```
