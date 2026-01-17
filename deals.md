---
layout: default
title: "Deals & Steals"
permalink: /deals/
---

<div class="deals-index">
    <h1 class="page-heading">Latest Deals</h1>
    <p>Unfiltered deals, savings strategies, and price glitches.</p>

    {% for deal in site.deals %}
    <div class="deal-container">
        <div class="deal-header">
            <h2 class="deal-title"><a href="{{ deal.url | relative_url }}" style="color: inherit; text-decoration: none;">{{ deal.title }}</a></h2>
        </div>
        <div class="deal-main">
            <div class="deal-sidebar" style="border:none; width:auto; align-items:flex-start; padding:0;">
                <div class="deal-pricing" style="text-align:left;">
                    <span class="price-current">{{ deal.price }}</span>
                    {% if deal.list_price %}
                    <span class="price-list">{{ deal.list_price }}</span>
                    {% endif %}
                </div>
            </div>
            <div class="deal-content">
                <p>{{ deal.excerpt }}</p>
                <a href="{{ deal.url | relative_url }}" class="deal-button" style="width: auto; padding: 8px 16px; font-size: 1rem;">View Deal</a>
            </div>
        </div>
    </div>
    {% endfor %}
</div>
