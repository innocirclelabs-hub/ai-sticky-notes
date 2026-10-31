# Troubleshooting the colleague test

- **Local diagnostic fails:** preserve its non-sensitive check name/error. Re-download and verify the ZIP checksum. Do not install arbitrary forks or disable security software.
- **Port 8791 occupied:** another application/AI Sticky Notes instance is using it. This package refuses to stop unrelated processes. Stop the other instance through its own controls.
- **Tunnel exits / never READY:** verify your tunnel ID, dedicated credential reference and account permissions against OpenAI's official tunnel guide. A file reference must point to a dedicated credential file, not an entire environment/configuration file. Check network access and correct workspace scope.
- **Tunnel absent in ChatGPT:** your ChatGPT account/workspace must support custom MCP/tunnels, and the tunnel must be visible to that workspace. This is a platform/account permission issue to record during testing, not a reason to share the publisher's key.
- **Note visible but AI disconnected:** keep Setup active, install/enable your actual MCP connection, and explicitly ask to open AI Sticky Notes once in that conversation. A loopback note alone is not MCP pairing.
- **Existing notes missing after update:** do not delete storage or uninstall. Confirm the same Chrome profile, extension directory, ChatGPT conversation and local data directory.
- **Connection stops after sign-out/restart:** launch Setup again and start the saved connection. This prerelease deliberately does not install an auto-start service.
- **Unsigned application warning:** this developer prerelease is not code-signed. Verify the official download and checksum and make your own trust decision. Follow organizational policies; do not turn off protection.

Official guide: https://developers.openai.com/api/docs/guides/secure-mcp-tunnels

## Continuation

No candidates: confirm the exact same account, verified project and installation, and that the source group is active. A stale/expired preview must be reopened; do not force transfer by renaming jobs. An old conversation refusing an update after handoff is intentional. Group-specific rules are in `work_contexts`; select the intended job rather than combining every job's rules.
