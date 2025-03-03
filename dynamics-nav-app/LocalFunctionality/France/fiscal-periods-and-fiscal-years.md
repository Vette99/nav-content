---
    title: Fiscal Periods and Fiscal Years
    description: A fiscal year is typically divided into 12 monthly fiscal periods. In [!INCLUDE[navnow](../../includes/navnow_md.md)], you can have two fiscal years open at the same time.

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
# Fiscal Periods and Fiscal Years
A fiscal year is typically divided into 12 monthly fiscal periods. In [!INCLUDE[navnow](../../includes/navnow_md.md)], you can have two fiscal years open at the same time. You cannot create a third fiscal year if there are two fiscal years open.  

To close a fiscal year, you must close the accounting periods within that year.  

You can only reopen a closed accounting period if the period falls within an open fiscal year. For more information, see [How to: Close Years](how-to-close-years.md). You cannot reopen a closed fiscal year.  

## Closing Fiscal Periods and Fiscal Years  
After a fiscal year is complete, you must close the accounting periods within that fiscal year. This is to ensure that general ledger entries are not posted for that period. For more information, see [How to: Fiscally Close Accounting Periods](how-to-fiscally-close-years.md).  

A fiscal year can be closed if all of the following criteria are met:  

- The posting dates in the **User Setup** window and the **General Ledger Setup** window do not fall within the year that you are closing. For more information, see User Setup and General Ledger Setup.  

- The fiscal year has been closed using the **Close Year** function in the **Accounting Periods** window. For more information, see [Closing Years and Periods](../../year-close-years-periods.md).  

- All of the unposted journal lines and simulation entries for the year have been posted or deleted.  

- All closing entries are up to date.  

When you close a fiscal period, the earliest open fiscal period is closed. The **Allow Posting From** field in the **General Ledger Setup** window is updated with the start date for the next open period, if the existing date in this field is not already a later date. If the **Allow Posting To** field in the **General Ledger Setup** window is within the closed period, then the value in the **Allow Posting To** field is updated with the end date for the first open fiscal period. For more information, see General Ledger Setup.  

At the end of the year, you must do the following:  

- Close the fiscal year using the **Close Year** function.  
- Generate a year-end closing entry.  
- Post the year-end closing entry, along with the offset equity account entries.  
- Close the fiscal year using the **Fiscally Close Year** function.  

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[How to: Post the Year-End Closing Entry](how-to-post-the-year-end-closing-entry.md)   
 [How to: Fiscally Close Accounting Periods](how-to-fiscally-close-accounting-periods.md)   
 [Closing Years and Periods](../../year-close-years-periods.md)   
 [How to: Post the Year-End Closing Entry](how-to-post-the-year-end-closing-entry.md)   
 [How to: Fiscally Close Years](how-to-fiscally-close-years.md)   
 [How to: Reopen Accounting Periods](how-to-reopen-accounting-periods.md)   
 [How to: Close Income Statement Accounts](how-to-close-income-statement-accounts.md)   
 [France Local Functionality](france-local-functionality.md)
