---
title: Копирование профиля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424730"
---
# <a name="copying-a-profile"></a>Копирование профиля

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Один из способов создания профиля — копирование из существующего профиля и изменение необходимых служб и поставщиков сообщений. Копирование профиля предполагает использование объекта администрирования профиля, предоставленного MAPI с помощью [функции MAPIAdminProfiles.](mapiadminprofiles.md) 
  
 **Копирование профиля**
  
1. Вызов **MAPIAdminProfiles** для получения **указателя интерфейса IProfAdmin.** 
    
2. Вызов [IProfAdmin::GetProfileTable,](iprofadmin-getprofiletable.md) чтобы получить доступ к таблице профилей. 
    
3. Создайте ограничение свойств со структурой [SPropertyRestriction,](spropertyrestriction.md) **чтобы** соответствовать PR_DISPLAY_NAME [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)с именем скопированного профиля. 
    
4. Вызов [IMAPITable::FindRow,](imapitable-findrow.md) чтобы найти соответствующую строку в таблице профилей. 
    
5. Вызов [IProfAdmin::CopyProfile,](iprofadmin-copyprofile.md) **передавая** значение столбца PR_DISPLAY_NAME как параметр _lpszOldProfileName._ 
    

