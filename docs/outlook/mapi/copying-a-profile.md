---
title: Копирование профиля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 77c7853c07830804aaa044f08078d95785bcfda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808204"
---
# <a name="copying-a-profile"></a>Копирование профиля

  
  
**Применимо к**: Outlook 
  
— Это один из способов создать профиль для копирования из существующего профиля и измените необходимые сообщения служб и поставщиков услуг. Копирование профиль включает использование объект администрирования профилей, предоставляемые MAPI через функцию [MAPIAdminProfiles](mapiadminprofiles.md) . 
  
 **Чтобы скопировать в профиль**
  
1. Вызов **MAPIAdminProfiles** для получения указателя интерфейса **IProfAdmin** . 
    
2. Вызов [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) для доступа к таблице профилей. 
    
3. Выполните построение ограничение свойства с [SPropertyRestriction](spropertyrestriction.md) структурой в соответствии с **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) с именем профиля для копирования. 
    
4. Вызовите [IMAPITable::FindRow](imapitable-findrow.md) , чтобы найти соответствующую строку в таблице профилей. 
    
5. Вызовите [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), передает значение столбца **PR_DISPLAY_NAME** в качестве параметра _lpszOldProfileName_ . 
    

