---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: de31fe7d472b143ed8f3c108dca84a019b5ce103
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357297"
---
# <a name="mapiinit_0"></a>MAPIINIT_0

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Передает параметры функции [MAPIInitialize.](mapiinitialize.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIX. H  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a>"Участники"

 **ulVersion**
  
> Integer value that represents the version number of the **MAPIINIT_0** structure. Член **ulVersion** для будущего расширения и не представляет версию интерфейса MAPI. В настоящее **время для ulVersion** необходимо установить MAPI_INIT_VERSION. 
    
 **ulFlags**
  
> Битмаска флагов, используемая для управления инициализацией сеанса MAPI. Можно установить следующие флаги:
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI должна создавать уведомления с помощью потока, посвященного обработке уведомлений, а не первого потока, используемого для вызова **MAPIInitialize.**
    
MAPI_NT_SERVICE 
  
> Вызываемая служба работает в качестве Windows службы. Вызыватели, которые не работают в качестве Windows службы, не должны устанавливать этот флаг; Вызыватели, работающие в качестве службы, должны установить этот флаг.
    
MAPI_NO_COINIT
  
> Установите флаг MAPI_NO_COINT, чтобы **MAPIInitialize** не пытался инициализировать COM с помощью вызова [coInitialize.](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx) Если **структура MAPIINIT_0** **в MAPIInitialize** с набором  _ulFlags_ для MAPI_NO_COINIT, MAPI предполагает, что com уже инициализирован и будет обходить вызов **в CoInitialize**.
    
## <a name="remarks"></a>Примечания

Многоуровневые клиенты должны установить флаг MAPI_MULTITHREAD_NOTIFICATIONS. Если флаг не установлен, в потоке, используемом для первого вызова **MAPIInitialize,** создаются уведомления. 
  
Дополнительные сведения о том, когда установить этот флаг и как реализовать безопасность потоков в клиенте, см. в этой [информации.](threading-in-mapi.md) 
  
## <a name="see-also"></a>См. также



[MAPIInitialize](mapiinitialize.md)


[Структуры MAPI](mapi-structures.md)

