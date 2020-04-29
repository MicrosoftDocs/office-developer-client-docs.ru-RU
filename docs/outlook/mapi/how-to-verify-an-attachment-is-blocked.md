---
title: Проверка блокировки вложения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: c1c6f960f2e24108bebdc8f6cbf08bf1d94d85ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345887"
---
# <a name="verify-an-attachment-is-blocked"></a><span data-ttu-id="5f756-103">Проверка блокировки вложения</span><span class="sxs-lookup"><span data-stu-id="5f756-103">Verify an attachment is blocked</span></span>

<span data-ttu-id="5f756-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f756-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f756-105">В этом примере кода на языке C++ показано, как использовать интерфейс [иаттачментсекурити: IUnknown](iattachmentsecurityiunknown.md) для определения того, блокируется ли вложение microsoft Outlook 2010 или microsoft Outlook 2013 для просмотра и индексирования.</span><span class="sxs-lookup"><span data-stu-id="5f756-105">This code sample in C++ shows how to use the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface to find out whether an attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span> 
  
<span data-ttu-id="5f756-106">[Иаттачментсекурити: IUnknown](iattachmentsecurityiunknown.md) является производным от интерфейса [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5f756-106">[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) is derived from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="5f756-107">Вы можете получить интерфейс [иаттачментсекурити: IUnknown](iattachmentsecurityiunknown.md) , вызвав метод [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) объекта Session для MAPI, запрашивая **IID_IAttachmentSecurity**.</span><span class="sxs-lookup"><span data-stu-id="5f756-107">You can obtain the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface by calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the MAPI session object, requesting **IID_IAttachmentSecurity**.</span></span> <span data-ttu-id="5f756-108">[Иаттачментсекурити:: исаттачментблоккед](iattachmentsecurity-isattachmentblocked.md) возвращает **true** в _пфблоккед_ , если вложение считается небезопасным в Outlook 2010 или Outlook 2013, и заблокировано для просмотра и индексирования в Outlook 2010 или Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="5f756-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) returns **true** in  _pfBlocked_ if the attachment is considered unsafe by Outlook 2010 or Outlook 2013 and is blocked for viewing and indexing in Outlook 2010 or Outlook 2013.</span></span> 
  
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


