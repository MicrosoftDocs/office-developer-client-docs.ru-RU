---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e7b3774d8dce446f0e87f041f11dac607f464680
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812479"
---
# <a name="tchar"></a>TCHAR

  
  
**Относится к**: Outlook 
  
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

