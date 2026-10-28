---
layout: page
permalink: /publications/
title: publications
description: # 
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->

<div class="publications">

<div class="pub-toolbar">
  <div class="pub-filter" role="group" aria-label="Publication filter">
    <button type="button" id="pub-filter-all">All</button>
    <button type="button" id="pub-filter-selected" class="active">Selected</button>
  </div>
  <div class="pub-scholar">
    <a href="https://scholar.google.com/citations?user=YXJ-_k0AAAAJ&hl=en" target="_blank" rel="noopener noreferrer">
      <i class="ai ai-google-scholar"></i> Google Scholar
    </a>
  </div>
</div>

{% bibliography -f {{ site.scholar.bibliography }} %}

</div>

<script>
  (function () {
    function applyPubFilter(mode) {
      document.querySelectorAll('.publications ol.bibliography > li').forEach(function (li) {
        var entry = li.querySelector('.pub-entry');
        var isSelected = entry && entry.classList.contains('pub-selected');
        li.style.display = (mode === 'all' || isSelected) ? '' : 'none';
      });
      // Hide year headings whose group has no visible entries
      document.querySelectorAll('.publications h2.bibliography').forEach(function (heading) {
        var list = heading.nextElementSibling;
        while (list && list.tagName !== 'OL') {
          list = list.nextElementSibling;
        }
        var anyVisible = false;
        if (list) {
          anyVisible = Array.prototype.some.call(list.children, function (li) {
            return li.style.display !== 'none';
          });
        }
        heading.style.display = anyVisible ? '' : 'none';
      });
      document.getElementById('pub-filter-all').classList.toggle('active', mode === 'all');
      document.getElementById('pub-filter-selected').classList.toggle('active', mode === 'selected');
    }

    function initPubFilter() {
      var allBtn = document.getElementById('pub-filter-all');
      var selectedBtn = document.getElementById('pub-filter-selected');
      if (!allBtn || !selectedBtn) return;
      allBtn.addEventListener('click', function () { applyPubFilter('all'); });
      selectedBtn.addEventListener('click', function () { applyPubFilter('selected'); });
      applyPubFilter('selected');
    }

    if (document.readyState === 'loading') {
      document.addEventListener('DOMContentLoaded', initPubFilter);
    } else {
      initPubFilter();
    }
  })();
</script>
