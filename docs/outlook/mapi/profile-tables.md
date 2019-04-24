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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328562"
---
# <a name="profile-tables"></a>Таблицы профилей

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В таблице Profile перечисляются сведения обо всех профилях, связанных с определенным клиентским приложением. Для каждого сеанса существует одна таблица профилей, реализованная MAPI для использования клиентами. 
  
Клиенты получают доступ к таблице профилей, вызывая метод [ипрофадмин:: жетпрофилетабле](iprofadmin-getprofiletable.md) . 
  
Таблица Profile является статической таблицей. Профили, помеченные для удаления, не включаются в таблицу профилей.
  
Как и в большинстве реализаций таблиц, если **жетпрофилетабле** вызывается, а для клиента нет доступных профилей, таблица создается с нулевым количеством строк. 
  
Следующие свойства составляют обязательный набор столбцов в таблицах профилей:
  
 **Пр_дефаулт_профиле** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

