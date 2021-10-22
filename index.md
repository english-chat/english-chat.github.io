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
    $.getJSON('http://api.allorigins.win/get?url=https%3A//netsplit.de/channels/details.php%3Froom%3D%2523%2523English%26net%3DLibera.Chat&callback=?', function (result){
      var parser = new DOMParser();
      var parsedhtml = parser.parseFromString(result.contents, "text/html");
	  var topic = parsedhtml.getElementsByTagName("td")[3].textContent.trim();
      wotd = topic.search("WotD:");
      wotd = topic.substring(wotd);
      $("#topic").text(wotd);
    });
  </script>

<a href="https://web.libera.chat/##English" class="button">Join now via webchat!</a><br/>
