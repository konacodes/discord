# Discord Library for Duck-lang

A quack-tastic Discord API library for building bots in Duck-lang!

## Installation

```bash
goose install konacodes/discord v0.1.0
```

## Usage

```duck
-- Import the discord library
quack [migrate "git+konacodes/discord" as dc]

-- Or import without namespace (functions become globals)
quack [migrate "git+konacodes/discord"]

-- Send a message
quack [let token be "YOUR_BOT_TOKEN"]
quack [dc.discord-send token "CHANNEL_ID" "Hello from Duck!"]
```

## Available Functions

### Messages
- `discord-send(token, channel-id, content)` - Send a message
- `discord-send-embed(token, channel-id, title, description, color)` - Send an embed
- `discord-reply(token, channel-id, message-id, content)` - Reply to a message

### Channels
- `discord-get-channel(token, channel-id)` - Get channel info
- `discord-get-messages(token, channel-id, limit)` - Get recent messages

### Users
- `discord-get-me(token)` - Get bot user info
- `discord-get-user(token, user-id)` - Get a user by ID

### Guilds
- `discord-get-guild(token, guild-id)` - Get guild info

### Reactions
- `discord-react(token, channel-id, message-id, emoji)` - Add a reaction

### Utilities
- `is-command(content, prefix)` - Check if message is a command
- `parse-command(content, prefix)` - Parse command and args
- `mention-user(user-id)` - Format a user mention
- `mention-channel(channel-id)` - Format a channel mention
- `mention-role(role-id)` - Format a role mention

### Colors
Pre-defined embed colors: `COLOR-RED`, `COLOR-GREEN`, `COLOR-BLUE`, `COLOR-YELLOW`, `COLOR-PURPLE`, `COLOR-ORANGE`, `COLOR-PINK`, `COLOR-DUCK`

## License

MIT - Quack freely!
