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
ms.openlocfilehash: e061808c57f25f881cc17fa5251e46ed5d524acd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809576"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
**Относится к**: Outlook 
  
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

