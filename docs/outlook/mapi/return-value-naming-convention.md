---
title: Return Value Naming Convention
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423617"
---
# <a name="return-value-naming-convention"></a>Return Value Naming Convention

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
The MAPICODE. Файл загона H содержит множество значений, которые клиент или поставщик услуг может вернуться из реализации метода интерфейса или увидеть возвращенные из вызова.
  
Коды, которые представляют условия предупреждения и сбоя, следуют другой конвенции именования, которая начинается с префикса MAPI, подчеркивания и W или E, чтобы указать тип кода. Остальная часть кода — это короткая строка символов для описания условия. Каждое слово в строке разделено подчеркиваемой строкой. Например, значение ошибки MAPI_E_TOO_COMPLEX, что реализация не может обрабатывать все, что запрашивалось в вызове. Значение предупреждения MAPI_W_PARTIAL_COMPLETION, что вызов удался, но возникли проблемы. Успешно выполнена только часть операции.
  

