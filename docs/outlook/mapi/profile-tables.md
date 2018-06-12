---
title: Профиль таблиц
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 84c2d02da840dfcad077462954cb10894ba153d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812063"
---
# <a name="profile-tables"></a>Профиль таблиц

  
  
**Применимо к**: Outlook 
  
В таблице профилей приведены сведения о всех профилей, связанных с определенной клиентским приложением. Существует одна таблица профиль для каждого сеанса реализован MAPI для использования клиентами. 
  
Для доступа клиентов к таблице профилей путем вызова метода [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) . 
  
В таблице профилей — это статическая таблица. Профили, помеченные для удаления не включаются в таблице профилей.
  
Как большинство реализаций таблицы, если называется **GetProfileTable** и нет профилей, доступных для клиента, создается таблица с нуля строк. 
  
Следующие свойства составляют обязательный столбец, задайте в таблицах профилей:
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

