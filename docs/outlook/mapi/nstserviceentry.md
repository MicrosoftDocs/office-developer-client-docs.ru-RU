---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96c04a242c477204ea1447fb78c31d189eeac59a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280056"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Функция точки входа службы сообщений для поставщика магазина MAPI, чтобы обернуть локальный магазин на основе PST в качестве магазина NST. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Реализовано в:  <br/> |Поставщик MAPI  <br/> |
|Вызывающая сторона:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT NSTServiceEntry( 
    HINSTANCE hInstance,   
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR * lppMapiError 
);
```

## <a name="parameters"></a>Parameters

 **NSTServiceEntry использует** прототип **[функции MSGSERVICEENTRY.](msgserviceentry.md)** Сведения о его параметрах см. в сайте **[MSGSERVICEENTRY.](msgserviceentry.md)** 
  
## <a name="return-values"></a>Возвращаемые значения

Сведения о значениях возврата см. в **[сайте MSGSERVICEENTRY.](msgserviceentry.md)** 
  
## <a name="remarks"></a>Примечания

При использовании **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** для получения адреса этой функции в msmapi32.dll в качестве имени процедуры укажите имя "NSTServiceEntry". 
  
Чтобы использовать API репликации, поставщик магазина MAPI должен сначала открыть и обернуть локальный магазин на основе PST, позвонив **[в NSTServiceEntry.](nstserviceentry.md)** Затем поставщик может использовать основные интерфейсы API, **[IOSTX](iostxiunknown.md)** и **[IPSTX](ipstxiunknown.md)** для выполнения репликации. 
  
Следующие замечания применяются к магазину NST:
  
- Не храните информацию в глобальном разделе профилей при реализации поставщика MAPI, который использует **NSTServiceEntry.** Раздел глобального профиля разделяется многими поставщиками, и данные, хранимые в этом профиле, могут быть перезаписаны. 
    
- Только элементы с существующими штампами времени изменения обновляются при их сэкономлении. 
    
- Проверка конфликтов не происходит автоматически при сэкономлении элементов.
    
-  При сэкономлении элементов не возникает дублирование обнаружения. 
    
-  Файл, представляющий кэшную версию сервера, примыкает к . NST. 
    
- Чтобы получить указатель в глобальном разделе профилей, служба сообщений вызывает **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** в объекте поддержки с помощью **pbNSTGlobalProfileSectionGuid,** как определено ниже: 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- В этом случае объект поддержки службы сообщений должен гарантировать, что **IMAPISupport::OpenProfileSection** **[](pidtagserviceuid-canonical-property.md)** возвращает раздел профилей, который определен свойством PR_SERVICE_UID в разделе профилей по умолчанию. Чтобы получить этот раздел профиля, объект поддержки может открыть раздел профилей по умолчанию, получить PR_SERVICE_UID и передать результат **в IMAPISupport::OpenProfileSection,** чтобы получить правильный глобальный раздел профилей. Объект поддержки, в свою очередь, возвращает указатель в этот глобальный профиль в службу сообщений. 
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)

