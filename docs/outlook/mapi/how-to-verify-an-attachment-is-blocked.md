---
title: Убедитесь, что Заблокированные вложения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: c1c6f960f2e24108bebdc8f6cbf08bf1d94d85ae
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393840"
---
# <a name="verify-an-attachment-is-blocked"></a><span data-ttu-id="fba59-103">Убедитесь, что Заблокированные вложения</span><span class="sxs-lookup"><span data-stu-id="fba59-103">Verify an attachment is blocked</span></span>

<span data-ttu-id="fba59-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fba59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fba59-105">Этот пример кода на C++ показано, как использовать [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) интерфейс, чтобы узнать, совместимо ли вложения блокируется Microsoft Outlook 2010 или Microsoft Outlook 2013 для просмотра и индексирования.</span><span class="sxs-lookup"><span data-stu-id="fba59-105">This code sample in C++ shows how to use the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface to find out whether an attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span> 
  
<span data-ttu-id="fba59-106">[IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) является производным от [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) интерфейс.</span><span class="sxs-lookup"><span data-stu-id="fba59-106">[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) is derived from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="fba59-107">Вы можете получить [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) интерфейс путем вызова [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) на объекте сеанса MAPI, запрашивающего **IID_IAttachmentSecurity**.</span><span class="sxs-lookup"><span data-stu-id="fba59-107">You can obtain the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface by calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the MAPI session object, requesting **IID_IAttachmentSecurity**.</span></span> <span data-ttu-id="fba59-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) возвращает **значение true** в _pfBlocked_ Если вложение считается небезопасных по Outlook 2010 или Outlook 2013 и заблокированные для просмотра и индексирования в Outlook 2010 или Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="fba59-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) returns **true** in  _pfBlocked_ if the attachment is considered unsafe by Outlook 2010 or Outlook 2013 and is blocked for viewing and indexing in Outlook 2010 or Outlook 2013.</span></span> 
  
```cpp
HRESULT IsAttachmentBlocked(LPMAPISESSION lpMAPISession, LPCWSTR pwszFileName, BOOL* pfBlocked) 
{ 
    if (!lpMAPISession || !pwszFileName || !pfBlocked) return MAPI_E_INVALID_PARAMETER; 
 
    HRESULT hRes = S_OK; 
    IAttachmentSecurity* lpAttachSec = NULL; 
    BOOL bBlocked = false; 
 
    hRes = lpMAPISession-&gt;QueryInterface(IID_IAttachmentSecurity,(void**)&amp;lpAttachSec); 
    if (SUCCEEDED(hRes) &amp;&amp; lpAttachSec) 
    { 
        hRes = lpAttachSec-&gt;IsAttachmentBlocked(pwszFileName,&amp;bBlocked); 
    } 
    if (lpAttachSec) lpAttachSec-&gt;Release(); 
 
    *pfBlocked = bBlocked; 
    return hRes; 
}

```


