---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: 'Дата последнего изменения: 23 июля 2011 г.'
localization_priority: Priority
ms.openlocfilehash: 2b04ebe6d05cd72a59fe6d44c9138468fd7ddec1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710449"
---
# <a name="tchar"></a>TCHAR

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Строка символов Win32, которая позволяет описать строки Юникода, ANSI или DBCS. Для платформ ANSI и DBCS TCHAR определяется так:
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a>Замечания

Для платформ Юникод TCHAR определяется как синоним типа WCHAR. 
  
Клиенты MAPI могут использовать тип данных TCHAR для представления строки типа char или WCHAR. Определите символьную константу UNICODE и ограничьте платформу при необходимости. MAPI интерпретирует данные платформы и внутренне преобразует TCHAR в соответствующую строку. Тип свойства MAPI, PT_TSTRING, работает так же, как и тип данных TCHAR. Если платформа поддерживает Юникод, свойствам типа PT_TSTRING назначается тип PT_UNICODE во время компиляции. Если платформа не поддерживает Юникод, этим свойствам назначается тип PT_STRING8.
  
Чтобы узнать больше об этой функции, просмотрите [кодировки](mapi-character-sets.md) и [список типов свойств](property-types.md). 
  
## <a name="see-also"></a>См. также



[Типы данных MAPI](mapi-data-types.md)

