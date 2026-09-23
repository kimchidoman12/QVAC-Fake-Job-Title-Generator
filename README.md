# QVAC Fake Job Title Generator

Type what you actually do and an on-device AI invents an absurdly fancy fake job title for it, with a deterministic pretentiousness meter.

## Run

```bash
npm install
npm start
```

Then open http://localhost:29364

## QVAC SDK version

`@qvac/sdk` ^0.19.0 (see `package.json`).

## How it works

Built on [Tether's QVAC SDK](https://www.npmjs.com/package/@qvac/sdk) — all inference runs on-device, no cloud call, no API key. The app loads `LLAMA_3_2_1B_INST_Q4_0` locally with `loadModel()`, generates with `completion()` (streamed via `tokenStream`), and releases the model with `unloadModel()` on shutdown.

## License

MIT
