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
ms.openlocfilehash: f7339588bcc6815545e7341eafffe9cf001c1d76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270030"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Уменьшает значение счетчика ссылок, очищает и удаляет глобальные данные для библиотеки MAPI DLL. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапикс. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a>Параметры

Нет 
  
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Клиентское приложение вызывает функцию **мапиунинитиализе** , чтобы завершить взаимодействие с MAPI, а затем вызовом функции [мапиинитиализе](mapiinitialize.md) . После вызова **мапиунинитиализе** клиент не может выполнять другие вызовы MAPI. 
  
 **Мапиунинитиализе** уменьшает значение счетчика ссылок, а соответствующая функция **мапиинитиализе** увеличивает значение счетчика ссылок. Таким образом, число вызовов одной функции должно равняться числу вызовов другой. 
  
> [!NOTE]
> Вы не можете вызывать **мапиинитиализе** или **Мапиунинитиализе** из функции Win32 **DllMain** или любой другой функции, создающей или завершающей потоки. Более подробную информацию можно узнать [в статье Использование потокобезопасных объектов](using-thread-safe-objects.md). 
  

