---
title: Атрибуты attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: f3319c9ae49fa97a6179b0ee800bd5dd594aefab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808087"
---
# <a name="attdate-attributes"></a>Атрибуты attDate

  
  
**Применимо к**: Outlook 
  
Все свойства MAPI, относящиеся к значения даты и времени, сопоставляются с TNEF атрибутов, начинающиеся с префикса **attDate** . Все эти кодируются как **DTR** структуры. Дата и время для атрибутов вложения, помеченные как также **DTR** структуры. 
  
Все свойства MAPI, относящиеся к значения даты и времени, сопоставляются с TNEF атрибутов, начинающиеся с префикса **attDate** . Все эти кодируются как **DTR** структуры. Дата и время для атрибутов вложения, помеченные как также **DTR** структуры. 
  
Структура **DTR** является очень похож на структуру **SYSTEMTIME** , определенных в файлы заголовков Win32. Структура **DTR** закодирован в потоке TNEF **sizeof(DTR)** байт, начиная с первого элемента структуры. Структура **DTR** определен в формате TNEF. Файл заголовка. 
  

