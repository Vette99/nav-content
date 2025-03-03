---
    title: How to Set Up 340 Reports for Small Businesses
    description: Use the following procedure to set up your business to report on a cash basis, that is, Cash Accounting Criteria (CAC). If you have not already done so, you can set up posting groups for cash-based VAT accounting for purchases and sales.

    documentationcenter: ''
    author: SorenGP

    ms.prod: "dynamics-nav-2018"
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 07/01/2017
    ms.author: edupont

---
# How to: Set Up 340 Reports for Small Businesses
Use the following procedure to set up your business to report on a cash basis, that is, Cash Accounting Criteria (CAC). If you have not already done so, you can set up posting groups for cash-based VAT accounting for purchases and sales.  

When you file a report 340, any transaction lines that are associated with unrealized VAT are assumed to have taken place under cash accounting.  

After VAT posting is set up to handle unrealized VAT, any printed sales order, purchase order, and so forth will be modified to have the following label in bold font added to the report just before the section reporting the document lines: **Régimen especial del criterio de caja**.  

## To set up reporting under CAC  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Setup**, and then choose the related link.  
2.  On the **General** FastTab, select the **Unrealized VAT** check box in the **General Ledger Setup** window. Choose the **OK** button.  
3.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **VAT Posting Setup**, and then choose the related link.  
4.  In the **VAT Posting Setup** window, select a group to modify or create a posting group that has general ledger accounts to treat the VAT amounts for the various unrealized VAT accounts in your VAT Posting Setup, and then choose the **Edit** action.  
5.  On the **General** FastTab, set the **Unrealized VAT Type** to **Percentage**.  
6.  On the **Sales** and **Purchase** FastTabs, specify general ledger accounts for the various **VAT Unreal. Account** fields.  

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[How to: Report VAT to Tax Authorities](../../finance-how-report-vat.md)
