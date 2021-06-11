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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Decrements the reference count, cleans up and deletes per-instance global data for the MAPI DLL. 
  
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

Клиентская заявка вызывает **функцию MAPIUninitialize,** чтобы прекратить взаимодействие с MAPI, начатое с вызова функции [MAPIInitialize.](mapiinitialize.md) После **вызова MAPIUninitialize** клиент не может делать другие вызовы MAPI. 
  
 **MAPIUninitialize** отнимет количество ссылок, а соответствующая функция **MAPIInitialize** прибавляет количество ссылок. Таким образом, количество вызовов одной функции должно равняться количеству вызовов другой. 
  
> [!NOTE]
> Вы не можете вызвать **MAPIInitialize** или **MAPIUninitialize** из функции **Win32 DllMain** или любой другой функции, которая создает или прекращает потоки. Дополнительные сведения см. в [Thread-Safe".](using-thread-safe-objects.md) 
  

