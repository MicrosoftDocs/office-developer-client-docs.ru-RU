---
title: Иексчанжемодифитаблежетластеррор
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350864"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает сведения о последней ошибке, произошедшей в объекте Table.
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a>Параметры

 _Состав_
  
> возврата Возвращаемое значение из метода, который завершился ошибкой.
    
 _ulFlags_
  
> возврата Не используется, установите значение 0 (ноль).
    
 _Лппмапиеррор_
  
> вышли Указывает на структуру MAPI [мапиеррор](mapierror.md) , которая содержит сведения о последней ошибке, произошедшей для объекта Table. 
    
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

