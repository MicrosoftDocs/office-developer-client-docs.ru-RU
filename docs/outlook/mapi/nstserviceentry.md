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
ms.openlocfilehash: b5902c25197c2ae5790e654a8f29227e107b4a72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810043"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

  
  
**Относится к**: Outlook 
  
Поставщик для упаковки в локальном хранилище на основе PST-файлов в качестве хранилище NST хранилища сообщений службы функцию точки входа для MAPI. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Реализованный:  <br/> |Поставщик MAPI  <br/> |
|Вызывается:  <br/> |MAPI  <br/> |
   
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

 **NSTServiceEntry** использует прототип функции **[MSGSERVICEENTRY](msgserviceentry.md)** . Сведения о его параметров содержатся **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="return-values"></a>Возвращаемые значения

Возвращаемые значения содержатся в разделе **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="remarks"></a>Замечания

При использовании **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** следует искать адреса этой функции msmapi32.dll, укажите «NSTServiceEntry» в качестве имени процедуры. 
  
Чтобы использовать API репликации, поставщик хранилища MAPI сначала необходимо открыть и перенос локального хранилища на основе PST-файлов, вызвав **[NSTServiceEntry](nstserviceentry.md)**. Поставщик затем можно использовать основные интерфейсы API, **[IOSTX](iostxiunknown.md)** и **[IPSTX](ipstxiunknown.md)**, чтобы выполнить репликацию. 
  
Следующие вычисляются в хранилище NST:
  
- Не следует хранить какие-либо сведения в разделе глобальные профиля, при реализации поставщика MAPI, который использует **NSTServiceEntry**. В разделе глобальные профилей совместно используемой многие поставщики и данных, хранящихся в этот профиль может быть перезаписана. 
    
- Только элементы с существующей отметки времени изменения получите их пометок обновлены при сохранении. 
    
- Проверка конфликтов не происходит автоматически при сохранении элементов.
    
-  Поиск повторяющихся данных не происходит при сохранении элементов. 
    
-  Добавляется файл, представляющий кэшированная версия сервера. NST. 
    
- Для получения указатель в разделе глобальные профилей, служба сообщений вызывает **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** в объекте поддержки с помощью **pbNSTGlobalProfileSectionGuid** , как указано ниже: 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- В этом случае объект поддержки службы сообщений следует убедиться, что **IMAPISupport::OpenProfileSection** возвращает раздела профиля, который идентифицируется свойством **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** в разделе профиля по умолчанию. Для получения в этом разделе профилей, объект поддержки можно откройте раздел профиля по умолчанию, получить **PR_SERVICE_UID**и передать результат в **IMAPISupport::OpenProfileSection** для получения раздела правильные глобальные профиля. Объект поддержки в свою очередь возвращает указатель на в этом разделе глобального профиля для службы сообщений. 
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)

