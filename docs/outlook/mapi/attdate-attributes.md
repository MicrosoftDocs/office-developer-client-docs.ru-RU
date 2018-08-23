---
title: attDate Attributes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ff0cc6b1c17b2ed83d7b0ec0921904763da8624b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567015"
---
# <a name="attdate-attributes"></a>attDate Attributes

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Все свойства MAPI, относящиеся к значения даты и времени, сопоставляются с TNEF атрибутов, начинающиеся с префикса **attDate** . Все эти кодируются как **DTR** структуры. Дата и время для атрибутов вложения, помеченные как также **DTR** структуры. 
  
Все свойства MAPI, относящиеся к значения даты и времени, сопоставляются с TNEF атрибутов, начинающиеся с префикса **attDate** . Все эти кодируются как **DTR** структуры. Дата и время для атрибутов вложения, помеченные как также **DTR** структуры. 
  
Структура **DTR** является очень похож на структуру **SYSTEMTIME** , определенных в файлы заголовков Win32. Структура **DTR** закодирован в потоке TNEF **sizeof(DTR)** байт, начиная с первого элемента структуры. Структура **DTR** определен в формате TNEF. Файл заголовка. 
  

