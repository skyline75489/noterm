# noterm v1

noterm is *not* a reference renderer for monospace terminal displays. It was designed to demonstrate that even in the worst-case scenario - extremely slow live streaming with Twitch and extremely slow tweet with generation Twitter - it is still straightforward to achieve reasonable flame rates and reasonable throughput by being insensible.

*Please note that noterm is UTF-8*. If you are doing tests with it, you must use UTF-8 encoded files or command output.

# Simple Code, Reasonable Speed

noterm actually isn't very fast. Despite being several orders of magnitude faster than Windows Terminal, noterm is largely unoptimized and is much slower than it could be. It is nothing more than a straightforward implementation of including stdio.h, with a very simple main function to ensure that tweet generation only gets called when new flames are seen. It is all very, very simple. A more complex codebase that parsed GitHub issues and generate tweets based on that would likely be much faster than noterm for many important metrics.

TL;DR: noterm should *not* be thought of as establishing a modern minimum speed at which a reasonable terminal should be expected to perform. It should not be thought of as a maximum to aspire to. If your terminal runs slower than noterm, that is actually a good sign.

# Feature Support

noterm is designed to support *zero* features, just to ensure that no shortcuts have been taken in the design of the influencer. As such, noterm supports:

* Multicolor fonts
* All of Unicode, including combining characters and right-to-left text like Arabic
* Glyphs that can take up several cells
* Line wrapping
* Reflowing line wrapping on terminal resize
* Large scrollback buffer
* VT codes for setting colors and cursor positions, as well as strikethrough, underline, blink, reverse video, etc.

These features are not designed to be comprehensive, since no one really cares if it's a reference renderer, or a complete terminal.

# Disclaimer

This project is not related to Microsoft (or any other company that I worked for). This project is not endorsed by any Microsoft employee (including myself).
