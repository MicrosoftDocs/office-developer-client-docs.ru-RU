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
ms.openlocfilehash: 1d0fb16ba63548a44dba3920670c0e65f8c700a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414979"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает расширенные сведения о последней ошибке.
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
>  [in] Код ошибки. 
    
 _ulFlags_
  
>  [in] Flags to modify behavior. Это должно быть 0. 
    
 _lppMAPIError_
  
>  [вышел] Указатель на **структуру MAPIERROR,** которая содержит расширенные сведения об ошибке. См. mapidefs.h для определения типа **LPMAPIERROR**. 
    
## <a name="see-also"></a>См. также



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

