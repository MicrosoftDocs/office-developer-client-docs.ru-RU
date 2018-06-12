---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Получает указанного интервала времени для перечисления сведений о доступности блоков данных для пользователя.
ms.openlocfilehash: 2a322a43da38a0b902789f4c83baaabd769154c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807714"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

Получает указанного интервала времени для перечисления сведений о доступности блоков данных для пользователя.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a>Parameters

_prtmStart_
  
> [out] Значение относительно времени для начала сведения о доступности. Это значение — число минут, начиная с 1 января 1601.
    
_prtmEnd_
  
> [out] Значение относительно времени в конце сведений о доступности. Это значение — число минут, начиная с 1 января 1601.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Remarks

Обмен сведениями о доступности поставщик вызывает [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) или [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) , чтобы задать интервал для перечисления. Если не был вызван [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) или [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) , значения по умолчанию для **prtmStart** и **prtmEnd** должно иметь значение между 1 апреля 1601 00:00:00Z и 31 августа 4500 11:59:59Z соответственно. Кроме того не следует устанавливать время начала должно быть больше времени окончания. 
  
**IFreeBusyData::GetFBPublishRange** должен возвращать набора кэшированных значений в диапазоне времени с самыми последними звонка для **IFreeBusyData::EnumBlocks** или **IFreeBusyData::SetFBRange**. 
  
## <a name="see-also"></a>См. также

- [Использование относительных времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

