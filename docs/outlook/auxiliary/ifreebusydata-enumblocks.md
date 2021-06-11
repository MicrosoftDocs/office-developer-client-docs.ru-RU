---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Получает интерфейс, который указывает свободные и загруженные блоки данных для пользователя в указанном диапазоне времени.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317558"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

Получает интерфейс, который указывает свободные и загруженные блоки данных для пользователя в указанном диапазоне времени.
  
## <a name="quick-info"></a>Краткие сведения

См. [iFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Parameters

_ppenumfb_
  
> [вышел] Интерфейс для переумерия бесплатных и занятых блоков.
    
_ftmStart_
  
> [in] Время начала для переумерия. Выражается в [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).
    
_ftmEnd_
  
> [in] Время окончания для переумерия. Выражается в **FILETIME**. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

Этот метод используется для указать диапазон времени элементов календаря, для которых можно получить сведения. Значения  *ftmStart* и *ftmEnd* кэшировать и возвращать в последующем вызове [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
Бесплатный/занятый поставщик также может впоследствии использовать возвращенный [интерфейс IEnumFBBlock](ienumfbblock.md) для доступа к переумериям. 
  
## <a name="see-also"></a>См. также

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [Использование относительного времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)

