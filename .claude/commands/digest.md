Generate an AI-powered social media digest using Screen Time Saver.

Run the following steps:

1. Check that `config.yaml` exists in the project root. If not, copy `config.example.yaml` to `config.yaml` and ask the user to configure their API key and sources.

2. Run the full pipeline. The simplest way is:

```bash
python app.py
```

This runs all 4 steps automatically: fetch, summarise, generate audio, and deliver.

3. If the user needs more control (specific style, no audio, delivery only), use the advanced CLI instead:
   - Default: `screen-time-saver generate --config config.yaml`
   - If the user says "no audio" or "text only": add `--no-audio`
   - If the user specifies a style (podcast/newsletter/briefing): add `--style <style>`
   - If the user says "deliver", "send", "call me", or "telegram": add `--deliver`

4. Report what was generated:
   - List the output files in `./output/`
   - If audio was generated, mention the MP3 file and its approximate duration
   - If delivery was requested, report the delivery status
   - Show a brief preview of the digest title and section headlines

User's request: $ARGUMENTS
