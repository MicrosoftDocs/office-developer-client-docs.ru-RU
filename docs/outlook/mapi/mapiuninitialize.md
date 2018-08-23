---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f95c86a137e7253f3445123c23f2dc0d76b6d87a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567393"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Уменьшает счетчик ссылок, очищает и удаления каждого экземпляра глобальных данных для библиотеки DLL MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a>Параметры

None 
  
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Клиентское приложение вызывает функцию **MAPIUninitialize** окончания его взаимодействия с MAPI, начиная с вызова функции [MAPIInitialize](mapiinitialize.md) . После вызова **MAPIUninitialize** нет других вызовов MAPI невозможны клиентом. 
  
 **MAPIUninitialize** уменьшает счетчик ссылок и соответствующую функцию **MAPIInitialize** увеличивает счетчик ссылок. Таким образом количество вызовов на одной функции должно совпадать с количеством вызовов в другой. 
  
> [!NOTE]
> В функции Win32 **DllMain** или любых других функций, который создает или завершение работы потоков не может вызывать **MAPIInitialize** или **MAPIUninitialize** из. Дополнительные сведения можно [С помощью объектов являющихся потокобезопасными](using-thread-safe-objects.md). 
  

