---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Возврат значения, для каждого указанного пользователя, интерфейс для перечисления сведений о доступности блоков данных в интервал времени.
ms.openlocfilehash: 9af5a40da9f0a831de7346b44cee9ca004c02300
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807717"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Возврат значения, для каждого указанного пользователя, интерфейс для перечисления сведений о доступности блоков данных в интервал времени. 
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IFreeBusySupport](ifreebusysupport.md).
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a>Parameters

_cMax_
  
> [in] Число интерфейсов [IFreeBusyData](ifreebusydata.md) для возврата. 
    
_rgfbuser_
  
> [in] Массив пользователей о доступности для извлечения данных.
    
_prgfbdata_
  
> [in] [out] Массив **IFreeBusyData** интерфейсы, которые соответствуют _rgfbuser_ массив структур [FBUser](fbuser.md) . 
    
   > [!NOTE]
   > Этот массив указателей, выделенный вызывающим абонентом и вызывающая. Фактические интерфейсов, на который указывает, снимаются, когда выполняется с их помощью вызывающего абонента. 
  
_phrStatus_
  
> [out] Массив **HRESULT** результатов для получения каждой соответствующий интерфейс **IFreeBusyData** . Значение может быть NULL. Результат имеет значение S_OK, если соответствующий _prgfbdata_ является допустимым. 
    
_pcRead_
  
>  [out] Фактическое число пользователей, для которых был найден интерфейс **IFreeBusyData** . 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="see-also"></a>См. также

- [Константы (занятости API)](constants-free-busy-api.md)

