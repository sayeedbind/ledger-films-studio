# ChatGPT setup

The workflow runs in any browser-capable chat. ChatGPT on Mac/Windows needs one setting first.

## The Full access setting

1. **Settings → General → Permissions → turn on Full access.**
2. Back in the chat, open the **permissions menu** in the message box and choose **Full access** for **this chat**. Turning it on in Settings only adds it to the menu; it does not switch the chat.
3. **Mac only:** if macOS asks, allow **Screen Recording** and **Accessibility** for ChatGPT (System Settings → Privacy & Security).

Without Full access you'll see errors like **"process launcher failed"**, **"browser-control session exited"** or **"process security error"**. When that happens: re-read the note the prompt shows, fix the setting, reply "done", and the agent starts a new browser session and continues from the next unfinished step. Finished clips are safe in My AI Videos.

If you don't see Full access, your plan or organization may not offer it. Use **Claude in Chrome** or the **Claude desktop app** instead — both run this workflow with no extra setting.

## Avoid the long-paste problem

ChatGPT turns long pasted messages into a file it then fails to open. The **SYSTEM_PROMPT.md** is short on purpose and loads the full playbook from this public repo, so nothing needs attaching.

If you want the whole thing to start every new chat automatically, make a **Project** or **custom GPT**:

1. Create the Project / GPT.
2. In **Instructions**, paste the SYSTEM_PROMPT.md contents (everything below the line).
3. Turn on browsing / the browser capability.
4. Start a chat and give only the format and story.

## Claude

- **Claude in Chrome** or the **Claude desktop app's** built-in browser: paste SYSTEM_PROMPT.md as the first message and follow the prompt.
- Claude skips the Full access note and starts on the intake question.
