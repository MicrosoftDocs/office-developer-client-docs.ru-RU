---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d4dc72309ff090317b2353cab0b4fc2c5be41181
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318216"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Флаги сообщений MAPI сопоставляются с флагами TNEF для сохранения обратной совместимости. Все флаги группируются и кодируются в одном байте. Используются следующие сопоставления:
  
|**Флаги сообщений MAPI**|**Флаги TNEF**|
|:-----|:-----|
|МСГФЛАГ_РЕАД  <br/> |Фмсреад  <br/> |
|МСГФЛАГ_УНМОДИФЕД  <br/> |~ Фмсмодифиед  <br/> |
|МСГФЛАГ_СУБМИТ  <br/> |Фмссубмиттед  <br/> |
|МСГФЛАГ_ХАСАТТАЧ  <br/> |Фмшасаттач  <br/> |
|МСГФЛАГ_УНСЕНТ  <br/> |Фмслокал  <br/> |
   
Эти флаги определены в формате TNEF. H файл заголовка.
  

