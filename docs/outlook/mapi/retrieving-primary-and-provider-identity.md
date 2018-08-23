---
title: Получение удостоверения поставщика и основного удостоверения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: da11cf684c4bdcfb94d33791ed7c61d2e322e1a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586587"
---
# <a name="retrieving-primary-and-provider-identity"></a>Получение удостоверения поставщика и основного удостоверения

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Поставщики услуг, обычно поставщиками адресных книг, имеют указать учетные данные, которые можно использовать для представления сеанса в различных ситуациях. Три свойства описывают поставщика удостоверений:
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
Эти свойства устанавливаются идентификатор записи, отображаемое имя и ключ поиска соответствующего объекта удостоверения, как правило, обмена мгновенными сообщениями пользователя. Поставщики, которые предоставить удостоверение также необходимо задать флаг STATUS_PRIMARY_IDENTITY в своем свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
  
В зависимости от потребностей можно использовать определенного поставщика удостоверений или основной идентификатор для сеанса. Также для отображения или для извлечения свойств, таких как **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)) можно использовать поставщика удостоверений. **PR_RESOURCE_PATH**, если значение, содержащее пути к файлам, используемые или созданные поставщиком. Извлечение свойства **PR_RESOURCE_PATH** для поставщика, передав основной идентификатор для поиска файлов, которые относятся к пользователя сеанса. 
  
 **Чтобы получить идентификатор определенного поставщика**
  
1. Вызов [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для доступа к таблице состояния. 
    
2. Выполните построение ограничение с помощью структуры [SPropertyRestriction](spropertyrestriction.md) в соответствии с столбце **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) с именем указанного поставщика. 
    
3. Вызов [IMAPITable::FindRow](imapitable-findrow.md) найдите строку поставщика. Поставщик удостоверений будет храниться в столбце **PR_IDENTITY_ENTRYID** , если он существует. 
    
 **Для извлечения основной идентификатор сеанса**
  
- Вызов [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** задает идентификатор сеанса на наличие STATUS_PRIMARY_IDENTITY значения в столбце **PR_RESOURCE_FLAGS** для одного из строки в таблице состояния. Если ни одна из строки состояния значение, **QueryIdentity** назначает удостоверение первого поставщика услуг, который задает три свойства PR_IDENTITY. Если нет поставщик удостоверений, **QueryIdentity** возвращает MAPI_W_NO_SERVICE. В этом случае необходимо создать строку знаков для представления универсальный пользователя, который может выступать в качестве основного удостоверения. 
    
 **Чтобы явно задать основной идентификатор сеанса**
  
- Вызов [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md). Передайте **MAPIUID** для поставщика услуг в целевой. 
    

