
# {{page.title}} <a class="pdf-link" href="{{page.pdf_url}}" target="_blank"><span class="mega-octicon octicon-file-pdf"></span></a>

This invoice is for work performed by _{{site.person_name}}_ as a
_{{site.person_title}}_ for GitHub.


__Invoice Number:__ {{ page.invoice_number }}  
__Date:__ {{ page.date | date_to_string }}  
__For period:__ {{ page.period }}  

## Service Fee Amounts

{% assign total = 0 %}
|__Description__|__Amount__|
|--|--:|{% for item in page.invoice_line_items %}{% assign total = total | plus:item.value %}
|{{item.title}}|{{item.value}} {{page.invoice_currency}}|{% endfor %}
|__Total:__|{{total}} {{page.invoice_currency}}|

## Bank/Wire Information

{{page.invoice_payment_info}}
