---
title: Убедитесь, что Заблокированные вложения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: a21383e0ea6920075a57d872e82851462bf0e8d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808637"
---
# <a name="verify-an-attachment-is-blocked"></a>Убедитесь, что Заблокированные вложения

**Применимо к**: Outlook 
  
Этот пример кода на C++ показано, как использовать [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) интерфейс, чтобы узнать, совместимо ли вложения блокируется Microsoft Outlook 2010 или Microsoft Outlook 2013 для просмотра и индексирования. 
  
[IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) является производным от [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) интерфейс. Вы можете получить [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) интерфейс путем вызова [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) на объекте сеанса MAPI, запрашивающего **IID_IAttachmentSecurity**. [IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) возвращает **значение true** в _pfBlocked_ Если вложение считается небезопасных по Outlook 2010 или Outlook 2013 и заблокированные для просмотра и индексирования в Outlook 2010 или Outlook 2013. 
  
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


