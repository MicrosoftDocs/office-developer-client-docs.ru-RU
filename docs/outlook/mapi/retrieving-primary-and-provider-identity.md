---
title: Искомые удостоверения основного и поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f59695eca2af71dd592c5b3a755d021ac53b3e31
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430814"
---
# <a name="retrieving-primary-and-provider-identity"></a>Искомые удостоверения основного и поставщика

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Поставщики услуг, как правило, поставщики адресных книг, могут предоставить удостоверение, которое можно использовать для представления сеанса в различных ситуациях. Три свойства описывают удостоверение поставщика:
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId)](pidtagidentityentryid-canonical-property.md) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay)](pidtagidentitydisplay-canonical-property.md) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey)](pidtagidentitysearchkey-canonical-property.md) 
    
Эти свойства устанавливаются для идентификатора записи, отображаемого имени и ключа поиска соответствующего объекта удостоверения, который обычно является пользователем системы обмена сообщениями. Поставщики, которые поставляют удостоверение, также устанавливают флаг STATUS_PRIMARY_IDENTITY в **свойстве PR_RESOURCE_FLAGS** ([PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)
  
В зависимости от потребностей можно использовать удостоверение конкретного поставщика или основное удостоверение для сеанса. Вы также можете использовать удостоверение поставщика для отображения или получения свойств, таких как **PR_RESOURCE_PATH** ([PidTagResourcePath).](pidtagresourcepath-canonical-property.md) **PR_RESOURCE_PATH**, если установлен, содержит путь к файлам, используемым или созданным поставщиком. Извлекает **PR_RESOURCE_PATH** поставщика, который сообщает основное удостоверение, если необходимо найти файлы, относящиеся к пользователю сеанса. 
  
 **Извлечение удостоверения определенного поставщика**
  
1. Вызов [IMAPISession::GetStatusTable для](imapisession-getstatustable.md) доступа к таблице состояния. 
    
2. Создайте ограничение, используя структуру [SPropertyRestriction,](spropertyrestriction.md) чтобы соответствовать столбце **PR_PROVIDER_DLL_NAME** [(PidTagProviderDllName)](pidtagproviderdllname-canonical-property.md)с именем указанного поставщика. 
    
3. Вызовите [IMAPITable::FindRow,](imapitable-findrow.md) чтобы найти строку поставщика. Удостоверение поставщика будет сохранено в  столбце PR_IDENTITY_ENTRYID, если оно существует. 
    
 **Извлечение основного удостоверения для сеанса**
  
- Вызов [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **Идентификатор сеанса QueryIdentity** зависит от наличия значения STATUS_PRIMARY_IDENTITY в столбце **PR_RESOURCE_FLAGS** для одной из строк в таблице состояния. Если ни одна из строк состояния не имеет этого значения, **QueryIdentity** назначает удостоверение первому поставщику службы, который задает три PR_IDENTITY свойства. Если ни один поставщик услуг не передает удостоверение, **QueryIdentity** возвращает MAPI_W_NO_SERVICE. В этом случае необходимо создать строку символов, представляющую универсального пользователя, который может служить основным удостоверением. 
    
 **Явное настройка основного удостоверения для сеанса**
  
- Вызовите [IMsgServiceAdmin::SetPrimaryIdentity.](imsgserviceadmin-setprimaryidentity.md) **Передав MAPIUID для** целевого поставщика услуг. 
    

