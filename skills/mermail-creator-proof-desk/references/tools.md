# Creator proof desk tool contracts

This skill composes existing Mermail tools. It adds no MCP tool ownership.

| Operation | Existing tools | Contract |
| --- | --- | --- |
| Resolve a workspace and mailbox | `list_workspaces`, `list_mailboxes`, `get_mailbox` | Reuse the exact authenticated workspace and a ready mailbox. Create nothing for public-only research. |
| Select an opportunity message | `search_emails`, `list_emails`, `get_email`, `get_email_context` | Start with metadata. Read only the selected clean message or bounded thread. |
| Save a proposal draft | `save_draft` | Use the exact mailbox and explicit recipient/subject/body. Saving is review-only and never sends. |
| Add or reuse a status label | `list_custom_labels`, `create_custom_label` | Create a label only when the owner requests inbox organization; do not claim that a label submits or tracks a bounty. |

Use native JSON objects for all MCP arguments. Prefer mailbox `public_id` and exact email/thread identifiers. Keep the source opportunity, public proof links, and draft identifier in the owner update, not in a public message.
