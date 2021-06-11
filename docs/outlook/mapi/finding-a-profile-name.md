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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Иногда клиентам необходимо найти имя профиля, используемого в настоящее время для сеанса, имя профиля по умолчанию или имя альтернативного профиля, установленного на компьютере.
  
Существует несколько способов получения имени профиля во время сеанса. Если необходимо найти имя профиля, которое не обязательно используется для сеанса, используйте первую процедуру. Если необходимо найти имя профиля по умолчанию, используйте вторую процедуру. Если необходимо найти имя текущего профиля сеанса, используйте последнюю процедуру. 
  
 **Поиск имени любого профиля**
  
1. Вызов [MAPIAdminProfiles](mapiadminprofiles.md) для получения **указателя интерфейса IProfAdmin.** 
    
2. Вызов [IProfAdmin::GetProfileTable,](iprofadmin-getprofiletable.md) чтобы получить доступ к таблице профилей. 
    
3. Вызовите метод [IMAPITable::QueryRows](imapitable-queryrows.md) таблицы профилей, чтобы получить все строки в таблице и изучить каждый из них, чтобы определить, представляет ли он целевой профиль. 
    
 **Поиск имени профиля по умолчанию**
  
1. Call [MAPIAdminProfiles](mapiadminprofiles.md).
    
2. Вызов [IProfAdmin::GetProfileTable,](iprofadmin-getprofiletable.md) чтобы получить доступ к таблице профилей. 
    
3. Создайте ограничение свойств со структурой [SPropertyRestriction,](spropertyrestriction.md) чтобы соответствовать PR_DEFAULT_PROFILE[(PidTagDefaultProfile)](pidtagdefaultprofile-canonical-property.md)со значением TRUE. 
    
4. Вызов [IMAPITable::FindRow,](imapitable-findrow.md) чтобы найти строку в таблице профилей, которая представляет профиль по умолчанию. Столбец **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)содержит имя профиля по умолчанию.
    
 **Поиск имени текущего профиля**
  
Чтобы найти имя текущего профиля, выполните один из следующих действий:
  
- Если у вас есть структура [MAPIUID,](mapiuid.md) представляющая один из разделов текущего профиля, передай его в  _параметре lpUID_ в [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md). Извлечение свойства **PR_PROFILE_NAME** раздела профилей [(PidTagProfileName)](pidtagprofilename-canonical-property.md)с помощью метода [IMAPIProp::GetProps.](imapiprop-getprops.md) 
    
- Позвоните [в IMAPISession::GetStatusTable,](imapisession-getstatustable.md) чтобы получить доступ к таблице состояния и найти строку с столбцом **PR_RESOURCE_TYPE** [(PidTagResourceType)](pidtagresourcetype-canonical-property.md)для MAPI_SUBSYSTEM. Столбец **PR_DISPLAY_NAME** этой строки — имя профиля. Не используйте таблицу состояния во время запуска, так как она блокирует приложение, пока пуллер MAPI не завершит инициализацию всех поставщиков транспорта. Это может привести к ухудшению производительности. 
    

