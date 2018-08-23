---
title: IPSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f45b070464fe1b3c177088ff6aa3295f961d45f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592593"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Получает расширенные сведения о последней ошибки.
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>Параметры

 _hResult_
  
>  [in] Код ошибки. 
    
 _ulFlags_
  
>  [in] Flags to modify behavior. Это должно быть равно 0. 
    
 _lppMAPIError_
  
>  [out] Указатель на структуру **MAPIERROR** , который содержит дополнительные сведения об ошибке. В разделе mapidefs.h для определения типа **LPMAPIERROR**. 
    
## <a name="see-also"></a>См. также



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

