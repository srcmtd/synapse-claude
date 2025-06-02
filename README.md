# synapse-claude

Vertex Synapse Rapid Power-Up for Anthropic Claude AI

## Setup

- If you haven't already, get an Anthropic [Console account][1]
- Create an [API Key][2]
- Clone this repo with `git clone https://github.com/srcmtd/synapse-claude.git`
- Install the package via the telepath API: `python -m synapse.tools.genpkg
  --push aha://cortex synapse-claude.yaml`
    - or via `python -m synapse.tools.genpkg --push cell:///vertex/storage synapse-claude.yaml`

## Usage

### `claude.setup.apikey`

Before you can use any `claude` commands, you'll need to set your API key
globally like this:

```
claude.setup.apikey <YOUR API KEY HERE>
```

Or if you only want to set your API key for yourself:

```
claude.setup.apikey --self <YOUR API KEY HERE>
```

### `claude.ask`

Pass a quoted string to `claude.ask` and it will be passed to Claude directly
as a prompt. The response will be printed.

```
storm> claude.ask "In the context of infosec, what is a Traffic Distribution System (TDS)?"
Sending prompt to Claude...
Claude Response:
==================================================
In the context of information security, a **Traffic Distribution System (TDS)**
is a malicious infrastructure component used by cybercriminals to intelligently
route and filter web traffic for illicit purposes.

## Key Functions of a TDS:

**Traffic Filtering & Routing:**
- Analyzes incoming web traffic based on various criteria (IP geolocation,
browser type, operating system, referrer, etc.)
...
```

## TODO

- [ ] `claude.ask`: Configurable Claude model (Claude 4 Opus, Claude 4 Sonnet,
  Claude 3.7 Sonnet) via `claude.setup.model` and a `--model` flag
- [ ] `claude.summarize` to summarize a report by passing in a `media:news`
  node, if `:file` is present
- [ ] `claude.transate --from RU --to EN` to translate articles from one
  language to another using Claude


[1]: https://console.anthropic.com/
[2]: https://console.anthropic.com/settings/keys
