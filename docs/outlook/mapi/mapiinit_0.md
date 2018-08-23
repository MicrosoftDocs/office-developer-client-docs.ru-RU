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
ms.openlocfilehash: 1eb4d7ac8d0287388a1bb76185f23636eddcf809
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591676"
---
# <a name="mapiinit0"></a>MAPIINIT_0

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Передает параметры в функцию [MAPIInitialize](mapiinitialize.md) . 
  
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

## <a name="members"></a>Members

 **ulVersion**
  
> Целочисленное значение, представляющее номер версии структуры **MAPIINIT_0** . Член **ulVersion** будущее расширение и не представляет версию интерфейса MAPI. На данный момент **ulVersion** должен иметь значение MAPI_INIT_VERSION. 
    
 **ulFlags**
  
> Битовая маска флаги, используемые для управления инициализации сеанса MAPI. Можно задать следующие флажки:
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI следует создавать с помощью потока, посвященного уведомлений обработки вместо первого потока, используемый для вызова **MAPIInitialize**уведомления.
    
MAPI_NT_SERVICE 
  
> Звонящий выполняется как служба Windows. Вызывающие объекты, которые не выполняется как служба Windows не следует устанавливать этот флаг; вызывающие объекты, на которых выполняется как служба необходимо установить этот флаг.
    
MAPI_NO_COINIT
  
> Задайте флаг MAPI_NO_COINT, чтобы **MAPIInitialize** не пытается инициализировать COM с помощью вызова [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx). Если структуры **MAPIINIT_0** передается в **MAPIInitialize** с _ulFlags_ , задайте значение MAPI_NO_COINIT, MAPI будет предполагать, что COM уже инициализирована и обходили вызова **CoInitialize**.
    
## <a name="remarks"></a>Замечания

Многопоточные клиентов следует устанавливать флаг MAPI_MULTITHREAD_NOTIFICATIONS. Если флажок не установлен, в потоке, используемом для первого вызова к **MAPIInitialize**создания уведомлений. 
  
Дополнительные сведения о реализации потокобезопасность в клиенте и когда установить этот флаг можно [Threading в MAPI](threading-in-mapi.md). 
  
## <a name="see-also"></a>См. также



[MAPIInitialize](mapiinitialize.md)


[Структуры MAPI](mapi-structures.md)

