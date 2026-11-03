# ssh_screenshot

Paste screenshots from your Mac into Claude Code running on another machine over ssh.

Press a key, select a screen area, and the image is uploaded to `~/screenshots` on your ssh host with its path copied to the clipboard. Paste the path into Claude Code there and it attaches the image.

## Setup

`ssh <host>` must work without a password prompt.

1. `git clone https://github.com/robin271828/ssh_screenshot.git ~/ssh_screenshot`
2. Shortcuts app → new shortcut → add a **Run Shell Script** action: `~/ssh_screenshot/ssh-screenshot <host>`
3. Shortcut details (ⓘ) → **Add Keyboard Shortcut**, e.g. Cmd+Shift+6
4. Shortcuts → Settings → Advanced → **Allow Running Scripts**, and grant Screen Recording when asked

List several hosts to send each screenshot to all of them; the clipboard gets the first one's path, and a host that does not answer within 5 seconds is skipped.
