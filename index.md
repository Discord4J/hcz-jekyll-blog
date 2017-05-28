---
layout: page
title: About
permalink: /
---

<!--TODO REPLACE HTML WITH MARKDOWN-->

<p>Discord4J is a wrapper for <a href="https://discordapp.com/">Discord's</a> <a href="https://discordapp.com/developers/docs/intro">websocket and REST API</a>.
It provides an easy-to-use implementation which has features suitable for both the most experienced and inexperienced Java programmers.
<p><h3>Why use Discord4J?</h3>
<p><ul>
      <li>Although not officially maintained or associated with Discord or Hammer & Chisel, it is <a href="https://discordapp.com/developers/docs/topics/libraries">officially recommended as a compliant API implementation</a>.</li>
      <li>Discord's bot api is fairly complicated, requiring the use of websockets in addition to REST calls in order to manage discord-related activities.
        Discord4J abstracts all of this and keeps an internal cache of data which is updated in real time, allowing for a reduction in REST calls which results in faster code.</li>
      <li>Discord4J is extensively multithreaded, allowing for operations to be executed quickly.</li>
      <li>There is an extensive event system. This allows for programs to be reactive to all sorts of situations asynchronously.</li>
      <li>Discord4J is extremely extensible thanks to its module system.</li>
      <li>There are many utility classes such as RequestBuffer which allows for automatic handling of ratelimits or RequestBuilder which provides a promise-like structure to logic (a la RxJava)</li>
      <li>Discord4J is still being actively developed by both its current maintainer, austinv11, and the community who provide invaluable feedback and pull-requests.
      This means it quickly gets updated to support the latest Discord changes (there are always a lot of them).</li>
      <li>We have our own <a href="https://discord.gg/NxGAeCY">Discord server!</a> Alternatively, we have a support channel on the <a href="https://discord.gg/0SBTUU1wZTU7PCok">Discord API server</a>.</li>
    </ul>
<p>For a more detailed explanation of the API, please take a look at its <a href="https://github.com/austinv11/Discord4J/blob/master/README.md">README on the Github repository</a>.