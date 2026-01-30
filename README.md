# LiveKit Agent

A voice AI project built with [LiveKit Agents for Python](https://github.com/livekit/agents) and [LiveKit Cloud](https://cloud.livekit.io/).



## Next steps

### Run and deploy your agent



**Get up and running** so you can start customizing:

1. **Install dependencies:**
   ```console
   uv sync
   ```

2. **Set up your LiveKit credentials:**
   
   Sign up for [LiveKit Cloud](https://cloud.livekit.io/), then configure your environment. You can either:
   
   - **Manual setup**: Copy to `.env.local` and fill in:
     - `LIVEKIT_URL`
     - `LIVEKIT_API_KEY`
     - `LIVEKIT_API_SECRET`
   
   - **Automatic setup** (recommended): Use the [LiveKit CLI](https://docs.livekit.io/home/cli/cli-setup):
     ```console
     lk cloud auth
     lk app env -w -d .env.local
     ```

3. **Download required models:**
   ```console
   uv run python src/agent.py download-files
   ```
   This downloads [Silero VAD](https://docs.livekit.io/agents/build/turns/vad/) and the [LiveKit turn detector](https://docs.livekit.io/agents/build/turns/turn-detector/) models.

4. **Test your agent:**
   ```console
   uv run python src/agent.py console
   ```
   This lets you speak to your agent directly in your terminal.

5. **Run for development:**
   ```console
   uv run python src/agent.py dev
   ```
   Use this when connecting to a frontend or telephony. This puts your agent into your LiveKit Cloud project, so use a different project if you don't want to affect production traffic.


