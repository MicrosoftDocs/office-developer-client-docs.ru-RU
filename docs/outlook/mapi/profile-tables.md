---
title: Таблицы профилей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1046c8d92feec16428329636257ed9c1f0ec8719
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571481"
---
# <a name="profile-tables"></a>Таблицы профилей

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
В таблице профилей приведены сведения о всех профилей, связанных с определенной клиентским приложением. Существует одна таблица профиль для каждого сеанса реализован MAPI для использования клиентами. 
  
Для доступа клиентов к таблице профилей путем вызова метода [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) . 
  
В таблице профилей — это статическая таблица. Профили, помеченные для удаления не включаются в таблице профилей.
  
Как большинство реализаций таблицы, если называется **GetProfileTable** и нет профилей, доступных для клиента, создается таблица с нуля строк. 
  
Следующие свойства составляют обязательный столбец, задайте в таблицах профилей:
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

