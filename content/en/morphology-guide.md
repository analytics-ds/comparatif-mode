---
title: "Body type guide for men and women"
description: "Find your body type in 4 quick questions and discover the cuts, sizes and brands suited to your silhouette. Free tool, no signup."
translationKey: "morphology-guide"
date: 2026-04-20
lastmod: 2026-04-20
---

<div class="morpho-tool">

<p class="morpho-intro">Answer 4 quick questions. The tool cross-checks shoulder, waist and hip measurements to identify your body type, then recommends suited cuts, sizes and brands.</p>

<form id="morpho-form" class="morpho-form" onsubmit="return false;">
  <fieldset>
    <legend>1. Gender</legend>
    <label><input type="radio" name="gender" value="h" checked> Man</label>
    <label><input type="radio" name="gender" value="f"> Woman</label>
  </fieldset>
  <fieldset>
    <legend>2. Shoulder measurement (cm)</legend>
    <input type="number" name="shoulders" min="60" max="150" value="110" required>
  </fieldset>
  <fieldset>
    <legend>3. Waist measurement (cm)</legend>
    <input type="number" name="waist" min="50" max="140" value="85" required>
  </fieldset>
  <fieldset>
    <legend>4. Hip measurement (cm)</legend>
    <input type="number" name="hips" min="70" max="150" value="100" required>
  </fieldset>
  <button type="button" class="btn-primary" onclick="morphoCalc()">Analyze my body type</button>
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
    if(s - h > 8) { type = 'V-shape body'; advice = 'Broad shoulders, narrow hips. Go for straight or slim cuts on the bottom and fitted tops. Recommended brands: Celio slim, Levi\'s 511, Jack & Jones slim fit.'; }
    else if(h - s > 8) { type = 'A-shape body'; advice = 'Hips wider than shoulders. Go for structured tops (shoulder-marked jackets) and straight or bootcut jeans. Recommended brands: Freeman T. Porter regular, Kaporal regular, Diesel bootcut.'; }
    else if(w >= s - 5) { type = 'O-shape body'; advice = 'Round silhouette, balanced shoulders and hips. Go for regular cuts and structured fabrics. Avoid slim. Recommended brands: Celio regular, Jules regular, Freeman T. Porter comfort fit.'; }
    else { type = 'H-shape body'; advice = 'Straight silhouette, shoulders and hips aligned. Anything works, favor straight cuts for a timeless style. Recommended brands: Levi\'s 501, Celio straight, Uniqlo regular, A.P.C. Petit Standard.'; }
  } else {
    if(h - s > 5) { type = 'A-shape (pear)'; advice = 'Hips wider than shoulders. Go for voluminous tops and straight or flare bottoms. Recommended brands: Sezane for tops, Levi\'s 501 straight, bootcut jeans.'; }
    else if(s - h > 5) { type = 'V-shape body'; advice = 'Shoulders wider than hips. Go for flare bottoms and clean tops. Recommended brands: Mango flare jeans, Freeman T. Porter flare, A-line dresses.'; }
    else if(w < s - 20 && w < h - 20) { type = 'X-shape (hourglass)'; advice = 'Defined waist, balanced shoulders and hips. Favor fitted cuts that highlight the waist. Recommended brands: Maje, Sezane, high-waist jeans.'; }
    else if(w >= s - 10) { type = 'O-shape body'; advice = 'Round silhouette, undefined waist. Go for flowing fabrics and straight cuts that elongate. Recommended brands: Cos, Uniqlo +J, straight dresses.'; }
    else { type = 'H-shape body'; advice = 'Straight silhouette, shoulder-waist-hip alignment. Favor structured cuts that create a waist. Recommended brands: The Kooples, Maje, wide belts.'; }
  }
  const r = document.getElementById('morpho-result');
  r.innerHTML = '<h3>' + type + '</h3><p>' + advice + '</p><p class="morpho-note">This analysis is indicative. Every silhouette is unique, fine-tune it in the fitting room.</p>';
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
