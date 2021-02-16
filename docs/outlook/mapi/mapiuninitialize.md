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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408525"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Убирает количество ссылок, очищает и удаляет глобальные данные для DLL MAPI для каждого экземпляра. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a>Параметры

Нет 
  
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Клиентские приложения вызывает функцию **MAPIUninitialize** для окончания взаимодействия с MAPI, начинается с вызова функции [MAPIInitialize.](mapiinitialize.md) После **вызова MAPIUninitialize** никакие другие вызовы MAPI не могут быть выполнены клиентом. 
  
 **MAPIUninitialize** понижет количество ссылок, а соответствующая функция **MAPIInitialize** добавит количество ссылок. Таким образом, число вызовов одной функции должно равняться числу вызовов другой. 
  
> [!NOTE]
> Невозможно вызвать **MAPIInitialize** или **MAPIUninitialize** из функции **Win32 DllMain** или любой другой функции, которая создает или завершает потоки. Дополнительные сведения см. в [Thread-Safe".](using-thread-safe-objects.md) 
  

