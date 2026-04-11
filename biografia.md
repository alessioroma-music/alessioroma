---
layout: page
title: "Biography"
permalink: /biography/
---

<div class="bio-portrait">
  <img src="{{ '/assets/images/alessio-roma-smile.jpg' | relative_url }}" alt="Alessio Roma, compositore">
</div>

<div class="bio-lang-toggle">
  <button class="bio-lang-btn" data-lang="it">IT</button>
  <span class="bio-lang-sep">|</span>
  <button class="bio-lang-btn active" data-lang="en">EN</button>
</div>

<div class="bio-text" id="bio-it" style="display:none" markdown="1">

Alessio Roma è un musicista e compositore nato a Bari nel 1993. 

Dopo una formazione strumentale come contrabbassista, ha intrapreso gli studi di composizione presso il Conservatorio di Musica "Niccolò Piccinni" di Bari sotto la guida di Biagio Putignano, conseguendo il diploma accademico di secondo livello nel marzo 2026. Ha frequentato masterclass internazionali di perfezionamento con Alessandro Melchiorre, Ivan Fedele, Giorgio Nottoli, Marco Stroppa, Robert HP Platz, Roberto Paci Dalò, Juha T. Koskinen e presso la Musikschule der Stadt Freising, in Germania.

Nel corso dei suoi studi ha approfondito le tecniche spettraliste — in particolare la poetica di Kaija Saariaho — e lo studio della fusione timbrica di più strumenti in un unico timbro percepibile, con riferimento al lavoro di compositori come Ivan Fedele. Nei suoi lavori integra spesso elementi extra-musicali, affrontando tematiche sociali e civili quali la salute mentale, l'oppressione dei popoli e la violenza sulle donne.

Le sue opere vengono eseguite in Italia e all'estero in concerti, festival e rassegne musicali. Ha partecipato agli eventi celebrativi per il centenario della Società Italiana di Musica Contemporanea con due prime esecuzioni assolute. Con *Cinque piccole variazioni per tromba* ha vinto il secondo premio al Concorso di composizione "Note per una stella" di Monteroni di Lecce (LE). Tra le commissioni ricevute, *Chiari Ombre* per violino e violoncello, commissionato dal Traetta Opera Festival (2025).

Collabora con il LEAP — Laboratorio ElettroAcustico Permanente di Roma, seguito da uno dei fondatori, Giuseppe Silvi. Le registrazioni delle sue composizioni sono pubblicate sulle principali piattaforme di streaming musicale.

</div>

<div class="bio-text" id="bio-en" markdown="1">

Alessio Roma is a musician and composer born in Bari in 1993. 

After training as a double bassist, he began studying composition at the "Niccolò Piccinni" Conservatory of Music in Bari with Biagio Putignano, earning his master's degree in March 2026. He attended international masterclasses with Alessandro Melchiorre, Ivan Fedele, Giorgio Nottoli, Marco Stroppa, Robert HP Platz, Roberto Paci Dalò, Juha T. Koskinen, and at the Musikschule der Stadt Freising in Germany.

During his studies, he delved into spectralist techniques—particularly the poetics of Kaija Saariaho—and the study of the timbral fusion of multiple instruments into a single perceptible timbre, drawing on the work of composers such as Ivan Fedele. In his works, he often integrates extra-musical elements, addressing social and civil issues such as mental health, the oppression of peoples, and violence against women.

His works are performed in Italy and abroad at concerts, festivals, and music events. He participated in the centennial celebrations of the Italian Society of Contemporary Music with two world premieres. With *Cinque piccole variazioni per tromba*, he won second prize at the "Note per una stella" composition competition in Monteroni di Lecce (LE). Among his commissions is *Chiari Ombre* for violin and cello, commissioned by the Traetta Opera Festival (2025).

He collaborates with LEAP—the Permanent Electroacoustic Laboratory in Rome—with one of its founders, Giuseppe Silvi. Recordings of his compositions are available on the main music streaming platforms.

</div>

<script>
  document.querySelectorAll('.bio-lang-btn').forEach(function(btn) {
    btn.addEventListener('click', function() {
      var lang = this.dataset.lang;
      document.querySelectorAll('.bio-lang-btn').forEach(function(b) { b.classList.remove('active'); });
      this.classList.add('active');
      document.getElementById('bio-it').style.display = lang === 'it' ? '' : 'none';
      document.getElementById('bio-en').style.display = lang === 'en' ? '' : 'none';
    });
  });
</script>
