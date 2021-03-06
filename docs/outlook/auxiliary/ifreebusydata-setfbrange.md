---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Задает диапазон времени для переумерия бесплатных и загруженных блоков данных для пользователя.
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421664"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

Задает диапазон времени для переумерия бесплатных и загруженных блоков данных для пользователя.
  
## <a name="quick-info"></a>Краткие сведения

См. [iFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a>Parameters

_rtmStart_
  
> [in] Относительное значение времени для начала получения бесплатных и загруженных сведений. Это число минут с 1 января 1601 г.
    
_rtmEnd_
  
> [in] Относительное значение времени для окончания бесплатных и загруженных сведений. Это число минут с 1 января 1601 г.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

Этот метод используется для указать диапазон времени элементов календаря, для которых можно получить сведения. Значения  *ftmStart*  и  *ftmEnd*  кэшировать и возвращать в последующем вызове [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
## <a name="see-also"></a>См. также

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [Использование относительного времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)

