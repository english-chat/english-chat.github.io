---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
auto-header: "Welcome to ##English on the Libera.Chat IRC network."
title: "Welcome"
icon: fa-door-open
order: 1
---

<div id="topic" style="margin-bottom: 30px;"></div>

  <script>
      $.getJSON('https://api.github.com/repos/english-chat/wotd/commits', function (result){
	  var topic = "WotD: "+result[0]['commit']['message'];
      wotd = topic.search("WotD:");
      wotd = topic.substring(wotd);

      var more = document.createElement('a');
      var linkText = document.createTextNode("See more WotD");
      more.appendChild(linkText);
      more.title = "See more WotD";
      more.href = "/wotd";

      var br = document.createElement('br');

      $("#topic").text(wotd);
      $("#topic").append(br);
      $("#topic").append(more);
    });
  </script>

<a href="https://web.libera.chat/##English" class="button">Join now via webchat!</a><br/>
