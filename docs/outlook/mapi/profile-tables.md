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
ms.openlocfilehash: 15c07c05af82389bce697c300cd9b1d504e98736
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424352"
---
# <a name="profile-tables"></a>Таблицы профилей

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В таблице профилей перечислены сведения обо всех профилях, связанных с определенным клиентом приложения. Существует одна таблица профилей для каждого сеанса, реализованная MAPI для использования клиентами. 
  
Клиенты получают доступ к таблице профилей, позвонив по [методу IProfAdmin::GetProfileTable.](iprofadmin-getprofiletable.md) 
  
Таблица профилей — это статическая таблица. Профили, помеченные для удаления, не включаются в таблицу профилей.
  
Как и в большинстве реализации таблицы, если **вызвана GetProfileTable** и нет профилей, доступных клиенту, таблица создается с нуля строк. 
  
Следующие свойства составляют необходимый столбец в таблицах профилей:
  
 **PR_DEFAULT_PROFILE** [(PidTagDefaultProfile)](pidtagdefaultprofile-canonical-property.md) 
  
 **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md) 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

