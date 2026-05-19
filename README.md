## Agentic CLI Setup

This guide provides instructions for setting up my "no BS" yet efficient agentic
environment. It's tailored to my personal preferences and requirements, which
aren't overly complex, used basically to automate boring stuff.

## Ollama and Models

Ollama is one of the easiest way to automate running models and setting up the
environment.

### Install Ollama

Run the following command in your terminal:

```
curl -s https://ollama.com/install.sh | bash
```

After installation, verify with:

```
ollama version
```

and start the service with:

```
ollama serve
```

#### Notes

- Make sure you have `curl` and `bash` installed.
- Ollama manages and serves models automatically, so you do not need to handle
  paths manually.
- If using via WSL make sure to have `systemd` enabled.
- For more advanced usage and CLI options, refer to the
  [Ollama Docs](https://docs.ollama.com).

### Install Models

Here we will be picking a very small model with `4b` params only. While that's
not the most optimal for large codebases, it works like a charm for quick tasks,
formatting, automating boring stuff, quick terminal commands and so on.

To install the model run:

```
ollama pull qwen3.5:4b-q4_K_M
```

Check the installed models with:

```
ollama list
```

To learn more about the model check
[qwen3.5:4b-q4_K_M](https://ollama.com/library/qwen3.5:4b-q4_K_M).

## Pi Code Agent

In it's own creator words:

> "Pi is a minimal terminal coding harness."

This is the tool I'm using currently as it's simple and quick to setup.

### Install Pi

Run the following command in your terminal:

```
curl -fsSL https://pi.dev/install.sh | sh
```

### Setup Pi

Pi can do alot, but what we are looking here it's simplicity. It's settings
could be found as JSON files at `~/.pi/agent/` directory, and to use my settings
basically copy the values from:

- [settings.json](./config/settings.json) → `~/.pi/agent/settings.json`,
- [models.json](./config/models.json) → `~/.pi/agent/models.json`

Those could be expanded or ovewritten at project level in a `.pi/` directory.

For further configuration and information check [pi.dev](https://pi.dev).

## Licence

This is an open-source project and is available under the
[**MIT License**](LICENSE). You are free to use, modify, and distribute the code
in accordance with the terms of the license.

## Contributors

If you run into any issues or have ideas for improvements, feel free to open an
issue or submit a pull request, or fork the project if you would prefer to take
it in your own direction.

[feliperdamaceno](https://github.com/feliperdamaceno)

## Contact me

Linkedin: [feliperdamaceno](https://www.linkedin.com/in/feliperdamaceno)
