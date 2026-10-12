# Rescue guides

Something broke. Find what you are seeing, and follow the steps in order.

## My AI tool says the MCP server has no tools

1. **Check the URL.** Copy it again from where you created the server. A missing
   character is the most common cause.
2. **Check the setting it went into.** Some tools want the URL itself; others want the
   name of a variable that holds a key. Putting a key where a name belongs fails
   quietly.
3. **Check the tool's own log.** Most AI tools have an MCP log or output panel. Look
   for the first error, not the last.
4. **Check private servers have a token.** A private server refuses requests without
   one, and some tools show that as "no tools" rather than an error.
5. **Restart the AI tool.** Many only load MCP servers on startup.

## It works on my computer but not online

1. **Missing settings.** Keys and passwords live in a `.env` file on your computer,
   which is never uploaded (on purpose). Add each one to your host's environment
   variables settings.
2. **Read the deploy log.** Your host shows a log for every deploy. Search for
   "error" and read the first one.
3. **Check the address.** Online, your app might live at a different web address than
   it did locally. Look for `localhost` in your code or settings.
4. **Ask your AI tool** with the exact error pasted in: "This works locally but fails
   on deploy with this error. Explain why before changing anything."

## My app forgot everything

1. **Is it saving anything at all?** Many hosts throw away files and memory between
   requests. Data that must last belongs in a database, not a file or a variable.
2. **Did the database change?** Ask your AI tool what database commands it ran
   recently. Some commands rebuild tables and lose data.
3. **For AI memory specifically:** a chat does not remember the last chat unless you
   store the history or connect persistent context. See
   [Why your AI keeps forgetting](02-why-context-matters.md).

## My bill spiked

1. **Find the service.** Check each provider's usage page: your AI model provider
   first, then your host, then your database.
2. **Look for a loop.** A workflow or function calling itself, or retrying forever,
   is the usual cause.
3. **Set limits now.** Most providers let you set a monthly spending limit or alert.
   Do it for every service with a card attached.
4. **Rotate exposed keys.** If a key was ever pasted into public code, someone else
   may be using it. Create a new one and delete the old one.

## My AI assistant makes things up

1. **Tell it to stay grounded.** Add to its instructions: "Only answer from the tool
   results. If they do not contain the answer, say so."
2. **Check it can reach the content.** Ask a question you know is covered. If that
   fails too, the problem is the connection, not the instructions.
3. **Check the content covers it.** If your docs do not say it, the assistant cannot
   know it. Add the content.

## Still stuck?

Ask in [Discussions](https://github.com/zthewriter/ship-with-ai/discussions) with
what you tried and the exact error message. Remove keys and passwords before pasting.
