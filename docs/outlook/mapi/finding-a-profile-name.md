---
title: Поиск имени профиля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b4efdd8d8238d4bc7e89a1153b9be34c7af76355
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407923"
---
# <a name="finding-a-profile-name"></a>Поиск имени профиля

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Иногда клиентам необходимо найти имя профиля, используемого в данный момент для сеанса, имя профиля по умолчанию или имя альтернативного профиля, установленного на компьютере.
  
Существует несколько способов получения имени профиля в ходе сеанса. Если необходимо найти имя профиля, которое необязательно является именем, используемым для сеанса, используйте первую процедуру. Чтобы найти имя профиля по умолчанию, используйте вторую процедуру. Если необходимо найти имя текущего профиля для сеанса, используйте последнюю процедуру. 
  
 **Поиск имени любого профиля**
  
1. Вызовите [MAPIAdminProfiles,](mapiadminprofiles.md) чтобы получить указатель интерфейса **IProfAdmin.** 
    
2. Вызовите [IProfAdmin::GetProfileTable,](iprofadmin-getprofiletable.md) чтобы получить доступ к таблице профилей. 
    
3. Вызовите метод [IMAPITable::QueryRows](imapitable-queryrows.md) таблицы профилей, чтобы получить все строки в таблице и проверить каждую из них, чтобы определить, представляет ли он целевой профиль. 
    
 **Поиск имени профиля по умолчанию**
  
1. Вызовите [MAPIAdminProfiles.](mapiadminprofiles.md)
    
2. Вызовите [IProfAdmin::GetProfileTable,](iprofadmin-getprofiletable.md) чтобы получить доступ к таблице профилей. 
    
3. Создайте ограничение свойства со структурой [SPropertyRestriction,](spropertyrestriction.md) чтобы соответствовать PR_DEFAULT_PROFILE **(** [PidTagDefaultProfile)](pidtagdefaultprofile-canonical-property.md)со значением TRUE.
    
4. Вызовите [IMAPITable::FindRow,](imapitable-findrow.md) чтобы найти строку в таблице профилей, которая представляет профиль по умолчанию. Столбец **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)содержит имя профиля по умолчанию.
    
 **Поиск имени текущего профиля**
  
Чтобы найти имя текущего профиля, выполните одно из следующих действий:
  
- Предположим, что у вас есть структура [MAPIUID,](mapiuid.md) представляющая один из разделов текущего профиля, передав его в _параметре lpUID_ [в IMAPISession::OpenProfileSection.](imapisession-openprofilesection.md) Получите свойство PR_PROFILE_NAME раздела **профиля** [(PidTagProfileName)](pidtagprofilename-canonical-property.md)с помощью метода [IMAPIProp::GetProps.](imapiprop-getprops.md) 
    
- Вызовите [IMAPISession::GetStatusTable,](imapisession-getstatustable.md) чтобы получить доступ к таблице состояния и найти строку, для столбца **PR_RESOURCE_TYPE** [(PidTagResourceType)](pidtagresourcetype-canonical-property.md)установлено значение MAPI_SUBSYSTEM. Столбец **PR_DISPLAY_NAME** для этой строки — это имя профиля. Не используйте таблицу состояния во время запуска, так как она блокирует приложение, пока пул mapI не завершит инициализацию всех поставщиков транспорта. Это может ухудшить производительность. 
    

