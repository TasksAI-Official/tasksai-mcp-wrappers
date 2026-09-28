# Troubleshooting

## The install command cannot run

If an AI assistant is running on the customer's Mac or Windows computer, ask it
to follow `AGENT-SETUP.md`. It can use the hash-verified native launcher when
Node.js is missing. A cloud-only assistant cannot configure a desktop app on the
customer's computer; use the Terminal route in `README.md` in that case.

## Browser connection does not open

Go to `https://teachertasksai.com/connect` and enter the connection code shown by the installer.

## The account is not found

Use the same email address used for TeacherTasksAI signup or purchase. Manual license-key entry is available only as a fallback.

## Tools do not appear

Restart your MCP client after installation. For Claude Desktop, start a new conversation after approving the connector.

## The workspace does not open

Run the manifest's doctor command for the same client used during installation.
Close an already-running TasksAI connection before an authorized update, and do
not remove the installation lock or saved workspace manually. Contact
support@teachertasksai.com with the doctor result if the check still fails.
