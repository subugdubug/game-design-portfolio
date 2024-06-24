---
layout: page
title: About Me
date: 2024-06-24
date_of_birth: 1994-11-09
date_crypto: 2017-01-01
---

<div class="image-with-caption">
  <img src="osaka-arcade.png" alt="Playing with a friend" style="filter: brightness(115%) drop-shadow(0px 0px 5px #000) saturate(115%);">
  <p class="caption">Slaying zombies at an Osaka arcade with a good friend.</p>
</div>

### Hi, I'm Raz. I'm <span id="age"></span> years old. I live in Tel Aviv, Israel with my wife.

There are many things that I like: Games (duh), music, weightlifting, distance running, film, cooking, coffee, and the list goes on (and gets weirder).

I've been building and designing systems in the Blockchain / Cryptocurrency / Web3 space for the past <span id="crypto_age"></span> years, where I first focused on research into protocols and decentralized consensus mechanisms, then moved on to more focused product management roles to create internal tooling, mostly focused around trading, data analysis and insight extraction.

After being on the other side as a gamer for as long as I can remember, and trying my hand at designing small-scale games, I realized this is what I want to devote most of my time towards. The greatest joy for me is to bring people together through play and get them to experience the highs and lows of a fun and engaging game.

Anyone who's played a well-designed game can share an account of the way they felt when things just _clicked_. For me, it happens most often when I play games made by [From Software](https://www.fromsoftware.jp/ww/). The combination of the 'play your own way' philosophy, combined with the excruciating difficulty makes the experience extremely rewarding and deeply etches it in your memory. Moreover, when playing these games with other people, there is a real sense of cooperation and achievement.

**These are the kinds of experiences I want to design and execute.**

I'm only starting out in my game design journey. I have a lot to learn, much to discover and many mistakes yet to make. I am excited for all of of those.

### Hit me up on:
- [Email](mailto:r@zpeleg.com)
- [Telegram](https://t.me/razpeleg)
- [LinkedIn](https://www.linkedin.com/in/razpeleg/)


<script>
  document.addEventListener("DOMContentLoaded", function() {
    function calculateAge(dateString) {
      var dob = new Date(dateString);
      var today = new Date();

      var age = today.getFullYear() - dob.getFullYear();
      var monthDiff = today.getMonth() - dob.getMonth();

      if (monthDiff < 0 || (monthDiff === 0 && today.getDate() < dob.getDate())) {
        age--;
      }

      return age;
    }

    var dateOfBirth = "{{ page.date_of_birth }}";
    var dateCrypto = "{{ page.date_crypto }}";

    var age = calculateAge(dateOfBirth);
    var cryptoAge = calculateAge(dateCrypto);

    document.getElementById("age").innerText = age;
    document.getElementById("crypto_age").innerText = cryptoAge;
  });
</script>
