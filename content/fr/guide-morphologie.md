---
title: "Guide morphologie homme et femme"
description: "Trouve ta morphologie en 4 questions et decouvre les coupes, tailles et marques adaptees a ta silhouette. Outil gratuit, sans inscription."
translationKey: "morphology-guide"
date: 2026-04-20
lastmod: 2026-04-20
---

<div class="morpho-tool">

<p class="morpho-intro">Reponds a 4 questions rapides. L'outil croise tour d'epaules, tour de taille et tour de hanches pour determiner ta morphologie, puis te recommande coupes, tailles et marques adaptees.</p>

<form id="morpho-form" class="morpho-form" onsubmit="return false;">
  <fieldset>
    <legend>1. Genre</legend>
    <label><input type="radio" name="gender" value="h" checked> Homme</label>
    <label><input type="radio" name="gender" value="f"> Femme</label>
  </fieldset>
  <fieldset>
    <legend>2. Tour d'epaules (cm)</legend>
    <input type="number" name="shoulders" min="60" max="150" value="110" required>
  </fieldset>
  <fieldset>
    <legend>3. Tour de taille (cm)</legend>
    <input type="number" name="waist" min="50" max="140" value="85" required>
  </fieldset>
  <fieldset>
    <legend>4. Tour de hanches (cm)</legend>
    <input type="number" name="hips" min="70" max="150" value="100" required>
  </fieldset>
  <button type="button" class="btn-primary" onclick="morphoCalc()">Analyser ma morphologie</button>
</form>

<div id="morpho-result" class="morpho-result" hidden></div>

</div>

<script>
function morphoCalc(){
  const f = document.getElementById('morpho-form');
  const g = f.gender.value;
  const s = +f.shoulders.value, w = +f.waist.value, h = +f.hips.value;
  let type = '', advice = '';
  if(g === 'h'){
    if(s - h > 8) { type = 'Morphologie en V'; advice = 'Epaules larges, hanches etroites. Privilegie les coupes droites ou slim pour le bas, les hauts pres du corps. Marques adaptees : Celio coupe slim, Levi\'s 511, Jack & Jones slim fit.'; }
    else if(h - s > 8) { type = 'Morphologie en A'; advice = 'Hanches plus larges que les epaules. Privilegie les hauts structures (vestes a epaules marquees) et les jeans droits ou bootcut. Marques adaptees : Freeman T. Porter regular, Kaporal regular, Diesel bootcut.'; }
    else if(w >= s - 5) { type = 'Morphologie en O'; advice = 'Silhouette ronde, carrure et bassin equilibres. Privilegie les coupes regular et les matieres structurantes. Evite le slim. Marques adaptees : Celio regular, Jules regular, Freeman T. Porter comfort fit.'; }
    else { type = 'Morphologie en H'; advice = 'Silhouette droite, epaules et hanches alignees. Tout te va, privilegie les coupes droites pour un style intemporel. Marques adaptees : Levi\'s 501, Celio straight, Uniqlo regular, A.P.C. Petit Standard.'; }
  } else {
    if(h - s > 5) { type = 'Morphologie en A (poire)'; advice = 'Hanches plus larges que les epaules. Privilegie les hauts volumineux et les bas droits ou evase. Marques adaptees : Sezane pour les hauts, Levi\'s 501 straight, jeans bootcut.'; }
    else if(s - h > 5) { type = 'Morphologie en V'; advice = 'Epaules plus larges que les hanches. Privilegie les bas evases et les hauts epures. Marques adaptees : Mango jeans flare, Freeman T. Porter flare, robes trapeze.'; }
    else if(w < s - 20 && w < h - 20) { type = 'Morphologie en X (sablier)'; advice = 'Taille marquee, epaules et hanches equilibrees. Privilegie les coupes cintrees qui soulignent la taille. Marques adaptees : Maje, Sezane, jeans taille haute.'; }
    else if(w >= s - 10) { type = 'Morphologie en O'; advice = 'Silhouette ronde, taille peu marquee. Privilegie les matieres fluides et les coupes droites qui allongent. Marques adaptees : Cos, Uniqlo +J, robes droites.'; }
    else { type = 'Morphologie en H'; advice = 'Silhouette droite, alignement epaules-taille-hanches. Privilegie les coupes structurees qui creent une taille. Marques adaptees : The Kooples, Maje, ceintures larges.'; }
  }
  const r = document.getElementById('morpho-result');
  r.innerHTML = '<h3>' + type + '</h3><p>' + advice + '</p><p class="morpho-note">Cette analyse est indicative. Chaque silhouette est unique, a affiner en cabine d\'essayage.</p>';
  r.hidden = false;
  r.scrollIntoView({behavior:'smooth', block:'start'});
  return false;
}
</script>

<style>
.morpho-tool { max-width: 720px; margin: 2rem auto; }
.morpho-intro { color: var(--text-light); margin-bottom: 2rem; }
.morpho-form fieldset { border: 1px solid var(--border); border-radius: var(--radius-md); padding: 1.2rem 1.5rem; margin-bottom: 1rem; }
.morpho-form legend { font-family: var(--font-ui); font-weight: 600; padding: 0 0.6rem; color: var(--primary); font-size: 0.95rem; }
.morpho-form label { margin-right: 2rem; font-family: var(--font-ui); }
.morpho-form input[type=number] { width: 100%; padding: 0.6rem 0.8rem; border: 1px solid var(--border); border-radius: var(--radius-sm); font-family: var(--font-ui); font-size: 1rem; }
.morpho-form button { margin-top: 1rem; width: 100%; }
.morpho-result { margin-top: 2.5rem; padding: 2rem; background: var(--background-alt); border-left: 4px solid var(--accent); border-radius: var(--radius-md); }
.morpho-result h3 { font-family: var(--font-heading); color: var(--primary); margin: 0 0 1rem; font-size: 1.6rem; }
.morpho-result p { margin: 0.6rem 0; color: var(--text); }
.morpho-note { font-size: 0.88rem; color: var(--text-light); font-style: italic; }
</style>
