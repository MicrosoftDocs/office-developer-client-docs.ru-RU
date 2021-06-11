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
ms.openlocfilehash: 8d5d4895e4440945896ee4f2212c5fca6da8610d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424513"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает сведения о последней ошибке, которая произошла в объекте таблицы.
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] Возвращаемого значения из сбойного метода.
    
 _ulFlags_
  
> [in] Не используется, установите значение 0 (ноль).
    
 _lppMAPIError_
  
> [вышел] Указывает на структуру [MAPI MAPIERROR, которая](mapierror.md) содержит сведения о последней ошибке, которая произошла для объекта таблицы. 
    
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

