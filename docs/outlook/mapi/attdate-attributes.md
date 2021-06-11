---
title: атрибуты attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408280"
---
# <a name="attdate-attributes"></a>атрибуты attDate

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Все свойства MAPI, относящиеся к датам и временим, соотносятся с атрибутами TNEF, которые имеют префикс **attDate.** Все они закодированы как **структуры DTR.** Даты и время для атрибутов вложений кодируются также как **структуры DTR.** 
  
Все свойства MAPI, относящиеся к датам и временим, соотносятся с атрибутами TNEF, которые имеют префикс **attDate.** Все они закодированы как **структуры DTR.** Даты и время для атрибутов вложений кодируются также как **структуры DTR.** 
  
Структура **DTR** очень похожа на структуру **SYSTEMTIME,** определяемую в файлах заголовки Win32. Структура **DTR** закодирована в потоке TNEF в качестве **bytes sizeof (DTR),** начиная с первого члена структуры. Структура **DTR** определяется в TNEF. Файл заглавной папки H. 
  

