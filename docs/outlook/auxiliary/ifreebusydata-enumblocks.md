---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Получает интерфейс, который перечисляет занятости блоков данных для пользователя в рамках в заданном диапазоне времени.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394540"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

Получает интерфейс, который перечисляет занятости блоков данных для пользователя в рамках в заданном диапазоне времени.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Параметры

_ppenumfb_
  
> [out] Интерфейс для перечисления блоки сведениям о доступности.
    
_ftmStart_
  
> [in] Время начала для перечисления. Выражается в [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).
    
_ftmEnd_
  
> [in] Время окончания для перечисления. Выражается в **FILETIME**. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Remarks

Этот метод используется для указания диапазона времени для элементов календаря, для которого нужно извлечь подробные сведения. Значения *ftmStart* и *ftmEnd* кэширования и возвращаются в последующих вызовов из [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
Обмен сведениями о доступности поставщика можно также последовательно использовать возвращенный интерфейс [IEnumFBBlock](ienumfbblock.md) для доступа к перечисления. 
  
## <a name="see-also"></a>См. также

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [Использование относительного времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)

