---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f0d2ad118346dd06788af972b64b10d6f6f6d0fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594294"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает сведения о, последнюю ошибку в объекте таблицы.
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a>Параметры

 _hResult_
  
> [in] Значение, возвращаемое методом, который не удалось.
    
 _ulFlags_
  
> [in] Не используется, задайте значение нуль (0).
    
 _lppMAPIError_
  
> [out] Указывает на MAPI [MAPIERROR](mapierror.md) структура, содержащая сведения о последней ошибки, которые произошли для объекта в таблице. 
    
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

