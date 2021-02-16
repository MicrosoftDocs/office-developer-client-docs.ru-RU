---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Получает заранее заранее задав диапазон времени для перенамерения блоков данных о занятости для пользователя.
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430079"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

Получает заранее заранее задав диапазон времени для перенамерения блоков данных о занятости для пользователя.
  
## <a name="quick-info"></a>Краткие сведения

См. [IFreeBusyData.](ifreebusydata.md)
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a>Параметры

_prtmStart_
  
> [out] Относительное значение времени начала сведений о занятости. Это значение является числом минут с 1 января 1601 г.
    
_prtmEnd_
  
> [out] Относительное значение времени для окончания сведений о занятости. Это значение — количество минут с 1 января 1601 г.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

Поставщик услуг занятости вызывает [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) или [IFreeBusyData::SetFBRange,](ifreebusydata-setfbrange.md) чтобы установить диапазон времени для нумерации. Если не был вызван [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) или [IFreeBusyData::SetFBRange,](ifreebusydata-setfbrange.md) значения по умолчанию для **prtmStart** и **prtmEnd** должны быть заданы между 1 апреля 1601 г. 00:00:00Z и 31 августа 4500 11:59:59Z соответственно. Кроме того, не следует устанавливать время начала больше времени окончания. 
  
**IFreeBusyData::GetFBPublishRange** должен возвращать кэшданные значения для диапазона времени, заданного последним вызовом **IFreeBusyData::EnumBlocks** или **IFreeBusyData::SetFBRange**. 
  
## <a name="see-also"></a>См. также

- [Использование относительного времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

