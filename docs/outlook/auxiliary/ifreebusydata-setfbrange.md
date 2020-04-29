---
title: ифрибусидатасетфбранже
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Задает диапазон времени для перечисления свободных и занятых блоков данных для пользователя.
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421664"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

Задает диапазон времени для перечисления свободных и занятых блоков данных для пользователя.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [ифрибусидата](ifreebusydata.md).
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a>Параметры

_ртмстарт_
  
> возврата Относительное значение времени начала сведений о занятости. Это значение равно количеству минут, прошедших с 1 января 1601 г.
    
_ртменд_
  
> возврата Относительное значение времени завершения сведений о занятости. Это значение равно количеству минут, прошедших с 1 января 1601 г.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

Этот метод используется для указания диапазона времени элементов календаря, сведения о котором требуется получить. Значения *фтмстарт* и *фтменд* кэшируются и возвращаются при последующих вызовах [ифрибусидата:: жетфбпублишранже](ifreebusydata-getfbpublishrange.md).
  
## <a name="see-also"></a>См. также

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [Использование относительного времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)

