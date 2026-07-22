# Getting Started

Get up and running with **Zero** in a few minutes.

## Prerequisites

- Python 3.10+ (or Node.js 18+ if you use the JS client)
- An API key from your [Neurobeat dashboard](https://docs.neurobeat.com)

## Install

=== "Python"

    ```bash
    pip install neurobeat-zero
    ```

=== "JavaScript"

    ```bash
    npm install @neurobeat/zero
    ```

## Configure

Set your API key as an environment variable:

```bash
export NEUROBEAT_API_KEY="your-api-key-here"
```

!!! warning
    Never commit your API key to version control. Use environment variables or a secrets manager.

## Your first request

=== "Python"

    ```python
    from neurobeat import Zero

    client = Zero()  # reads NEUROBEAT_API_KEY from the environment

    response = client.run(
        task="hello-world",
        input={"message": "Hello, Zero!"},
    )

    print(response.output)
    ```

=== "JavaScript"

    ```javascript
    import { Zero } from "@neurobeat/zero";

    const client = new Zero(); // reads NEUROBEAT_API_KEY from the environment

    const response = await client.run({
      task: "hello-world",
      input: { message: "Hello, Zero!" },
    });

    console.log(response.output);
    ```

## Next steps

- Explore the [API reference](https://docs.neurobeat.com)
- Learn about [authentication and API keys](https://docs.neurobeat.com)
- Browse [example projects](https://docs.neurobeat.com)
