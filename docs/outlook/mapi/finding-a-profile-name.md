---
title: Поиск имени профиля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 332b78bcebbcd54de43376553ec4aea386c1c359
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808436"
---
# <a name="finding-a-profile-name"></a>Поиск имени профиля

  
  
**Применимо к**: Outlook 
  
Клиенты в некоторых случаях требуется найти имя профиля, используемого сейчас для сеанса, имя профиля по умолчанию или имя альтернативного профиля, установленный на компьютере.
  
Существует несколько способов получить имя профиля в ходе сеанса. Чтобы найти имя профиля, который не обязательно, используемый для сеанса, используйте первой процедуры. Если требуется найти имя профиля по умолчанию, используйте во второй процедуре. Чтобы найти имя текущего профиля для сеанса, используйте последнего действия. 
  
 **Чтобы найти имя любого профиля**
  
1. Вызов [MAPIAdminProfiles](mapiadminprofiles.md) для получения указателя интерфейса **IProfAdmin** . 
    
2. Вызов [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) для доступа к таблице профилей. 
    
3. Вызов метода [IMAPITable::QueryRows](imapitable-queryrows.md) в таблице профиля для извлечения все строки в таблице и проверить каждый из них для определения, если он представляет своего профиля целевой. 
    
 **Чтобы найти имя профиля по умолчанию**
  
1. Вызов [MAPIAdminProfiles](mapiadminprofiles.md).
    
2. Вызов [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) для доступа к таблице профилей. 
    
3. Выполните построение ограничение свойства с [SPropertyRestriction](spropertyrestriction.md) структурой в соответствии со значением TRUE **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)).
    
4. Вызов [IMAPITable::FindRow](imapitable-findrow.md) найдите строку в таблице профиля, который представляет профиля по умолчанию. В столбце **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) содержит имя профиля по умолчанию.
    
 **Чтобы найти имя текущего профиля**
  
Чтобы найти имя текущего профиля, выполните одно из следующих действий:
  
- Если предполагается, что у вас есть структура [MAPIUID](mapiuid.md) , представляющий один из разделов текущего профиля, передайте в него с помощью параметра _lpUID_ [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md). Получение свойства **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) в разделе профилей с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) . 
    
- Вызов [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для доступа к таблице состояния и найдите строку, задайте значение MAPI_SUBSYSTEM столбец **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)). В столбце **PR_DISPLAY_NAME** для этой строки — имя профиля. Не используйте в таблице состояния во время начала из-за его блокирует приложения до завершения инициализации всех поставщиков транспорта диспетчер очереди MAPI. Это может привести к снижению производительности. 
    

