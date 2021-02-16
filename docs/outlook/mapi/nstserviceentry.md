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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Функция точки входа службы сообщений для поставщика точки входа MAPI для переноса локального магазина на основе PST в NST-хранилище. 
  
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

## <a name="parameters"></a>Параметры

 **NSTServiceEntry использует** прототип **[функции MSGSERVICEENTRY.](msgserviceentry.md)** Сведения о его параметрах см. в **[msGSERVICEENTRY.](msgserviceentry.md)** 
  
## <a name="return-values"></a>Возвращаемые значения

Сведения о возвращаемом значении см. в **[msGSERVICEENTRY.](msgserviceentry.md)** 
  
## <a name="remarks"></a>Примечания

При использовании **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** для искомого адреса этой функции в msmapi32.dll укажите "NSTServiceEntry" в качестве имени процедуры. 
  
Чтобы использовать API репликации, поставщик магазина MAPI должен сначала открыть и завернуть локальное хранилище на основе PST, вызывая **[NSTServiceEntry.](nstserviceentry.md)** Затем поставщик может использовать основные интерфейсы API, **[IOSTX](iostxiunknown.md)** и **[IPSTX](ipstxiunknown.md)** для выполнения репликации. 
  
К NST- магазину применяются следующие замечания:
  
- Не храните информацию в разделе глобального профиля при реализации поставщика MAPI, который использует **NSTServiceEntry.** Раздел глобального профиля совместно с другими поставщиками, и данные, хранимые в этом профиле, могут быть перезаписаны. 
    
- Только элементы с существующими отметками времени изменения обновляют свои отметки при их экономии. 
    
- При сэкономлении элементов проверка конфликтов не происходит автоматически.
    
-  Повторяющиеся обнаружения не происходят при экономии элементов. 
    
-  Файл, представляющий кэшную версию сервера, будет к ним придан. NST. 
    
- Чтобы получить указатель на глобальный раздел профиля, служба сообщений вызывает **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** в объекте поддержки с помощью **pbNSTGlobalProfileSectionGuid,** как определено ниже: 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- В этом случае объект поддержки службы сообщений должен гарантировать, что **IMAPISupport::OpenProfileSection** возвращает раздел профиля, который определен свойством **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** в разделе профиля по умолчанию. Чтобы получить этот раздел профиля, объект поддержки может открыть раздел профиля по умолчанию, извлечь PR_SERVICE_UID и передать результат **в IMAPISupport::OpenProfileSection,** чтобы получить правильный раздел глобального профиля. Объект поддержки, в свою очередь, возвращает указатель на этот раздел глобального профиля службе сообщений. 
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)

