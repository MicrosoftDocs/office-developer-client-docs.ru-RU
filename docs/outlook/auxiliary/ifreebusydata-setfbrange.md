---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Задает диапазон времени для перечисления блоков данных о доступности для пользователя.
ms.openlocfilehash: 84a25a2dd43f594caa075d90e4f183086452184a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807732"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

Задает диапазон времени для перечисления блоков данных о доступности для пользователя.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a>Параметры

_rtmStart_
  
> [in] Значение относительно времени для начала сведения о доступности. Это значение — число минут, начиная с 1 января 1601.
    
_rtmEnd_
  
> [in] Значение относительно времени в конце сведений о доступности. Это значение — число минут, начиная с 1 января 1601.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Remarks

Этот метод используется для указания диапазона времени для элементов календаря, для которого нужно извлечь подробные сведения. Значения *ftmStart* и *ftmEnd* кэширования и возвращаются в последующих вызовов из [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
## <a name="see-also"></a>См. также

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [Использование относительного времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)

