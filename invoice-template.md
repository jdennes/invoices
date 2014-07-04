
# {{page.title }}

This invoice is for work performed by _{{site.person_name}}_ as a
_{{site.person_title}}_ for GitHub.


__Invoice Number:__ {{ page.invoice_number }}  
__Date:__ {{ page.date | date_to_string }}  
__For period:__ {{ page.period }}  

## Service Fee Amounts

|__Description__|__Amount__|
|--|--:|
|Monthly Salary|{{site.person_monthly_salary}} {{site.person_currency}}|
|Cell Phone Reimbursement|{{site.person_monthly_phone_reimbursement}} {{site.person_currency}}|
|__Total:__|{{site.person_monthly_salary | plus: site.person_monthly_phone_reimbursement}} {{site.person_currency}}|

## Bank/Wire Information

{{site.person_payment_info}}
