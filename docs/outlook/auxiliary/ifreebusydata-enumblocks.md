---
title: ифрибусидатаенумблоккс
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Получает интерфейс, который перечисляет блоки данных о занятости для пользователя в указанном диапазоне времени.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317558"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

Получает интерфейс, который перечисляет блоки данных о занятости для пользователя в указанном диапазоне времени.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [ифрибусидата](ifreebusydata.md).
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Параметры

_ппенумфб_
  
> вышли Интерфейс для перечисления блоков занятости.
    
_фтмстарт_
  
> возврата Время начала перечисления. Он выражается в [fileTime](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).
    
_фтменд_
  
> возврата Время окончания перечисления. Он выражается в **fileTime**. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

Этот метод используется для указания диапазона времени элементов календаря, сведения о котором требуется получить. Значения *фтмстарт* и *фтменд* кэшируются и возвращаются при последующих вызовах [ифрибусидата:: жетфбпублишранже](ifreebusydata-getfbpublishrange.md).
  
Поставщик сведений о доступности также может впоследствии использовать возвращенный интерфейс [иенумфбблокк](ienumfbblock.md) для доступа к перечислению. 
  
## <a name="see-also"></a>См. также

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [Использование относительного времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)

