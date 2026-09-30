# Your Next Tours MCP

Connect your AI assistant to your [Your Next Tours](https://yournext.tours) account. Your Next
Tours is a phone-based audio system for tour groups: the guide talks into the app, participants
listen from their own phones. This connector lets you prepare and manage everything around your
tours from Cursor, Claude, VS Code or any MCP client.

This repository contains only the client configuration (a Cursor plugin manifest). The MCP server
is a hosted service; there is nothing to install or run locally.

- **Server URL:** `https://api.yournext.tours/api/mcp/guide`
- **Transport:** Streamable HTTP
- **Auth:** OAuth 2.1 (sign in with your Your Next Tours account; your password is never shared
  with the assistant). A per-account API key can be created in the panel instead.
- **Setup guide:** https://yournext.tours/ai-assistant-integration/

## What you can do

- Tour templates and travel programs: create, edit, duplicate, reorder stops and slides
- Trips: create departures, add and invite participants, publish
- Tours and ratings: sessions, statistics, audience and feedback
- Company website (Enterprise): edit sections, upload images, translate, publish

Access follows the permissions you grant during sign-in and your role in your company. Actions
that notify participants, participant lists, forms and company management are only available with
an API key that explicitly includes those scopes.

## Install

**Cursor:** install the plugin from the Cursor Marketplace, or add to `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "your-next-tours": {
      "url": "https://api.yournext.tours/api/mcp/guide"
    }
  }
}
```

Cursor opens a browser window to sign in the first time you use it.

**Claude Code:**

```bash
claude mcp add --transport http your-next-tours https://api.yournext.tours/api/mcp/guide
```

**Claude (web/desktop) and other clients:** add a custom connector with the server URL above.

## Privacy

See the [privacy policy](https://yournext.tours/privacy-policy/). Every call made through the
connector is recorded in an audit log tied to your account. You can
disconnect at any time by revoking the connection or API key in the panel.

## Support

https://yournext.tours/ai-assistant-integration/
