---
title: Words of the Day
auto-header: use-title
layout: "page"
hide: true
---

This is a record of the words of the day used in the topic of ##English on Libera.Chat.

The record starts October 22, 2021.

<ul id="wotd_history"></ul>
  <script>
      $.getJSON('https://api.github.com/repos/english-chat/wotd/commits?since=2021-10-22T22:15:28Z', function (result){
      result.forEach(addWotd);

      function addWotd(item) {
         var wotd = document.createElement("li");
         wotd.style.margin = "30px";
         var wotdDef = document.createTextNode(item["commit"]["message"]);
         wotd.appendChild(wotdDef);
         document.getElementById("wotd_history").appendChild(wotd);
      }
    });
  </script>
