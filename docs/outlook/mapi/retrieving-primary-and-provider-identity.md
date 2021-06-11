---
title: Повторное иждивение удостоверения основного поставщика и поставщика
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
# <a name="retrieving-primary-and-provider-identity"></a>Повторное иждивение удостоверения основного поставщика и поставщика

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поставщики услуг, как правило, поставщики адресных книг, могут предоставить удостоверение, которое можно использовать для представления сеанса в различных ситуациях. Три свойства описывают удостоверение поставщика:
  
- **PR_IDENTITY_ENTRYID** [(PidTagIdentityEntryId)](pidtagidentityentryid-canonical-property.md) 
    
- **PR_IDENTITY_DISPLAY** [(PidTagIdentityDisplay)](pidtagidentitydisplay-canonical-property.md) 
    
- **PR_IDENTITY_SEARCH_KEY** [(PidTagIdentitySearchKey)](pidtagidentitysearchkey-canonical-property.md) 
    
Эти свойства за набором идентификатора записи, отображаемого имени и ключа поиска соответствующего объекта удостоверения, который обычно является пользователем обмена сообщениями. Поставщики, которые поставляют удостоверение, также задают флаг STATUS_PRIMARY_IDENTITY в **свойстве PR_RESOURCE_FLAGS** [(PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)
  
В зависимости от ваших потребностей можно использовать удостоверение конкретного поставщика или основное удостоверение для сеанса. Вы можете использовать удостоверение поставщика также для отображения или получения свойств, таких как **PR_RESOURCE_PATH** [(PidTagResourcePath).](pidtagresourcepath-canonical-property.md) **PR_RESOURCE_PATH,** если установлено, содержит путь к файлам, используемым или созданным поставщиком. **Извлечение PR_RESOURCE_PATH** для поставщика, снабжающего основной идентификатор, при поиске файлов, относящихся к пользователю сеанса. 
  
 **Для получения удостоверения конкретного поставщика**
  
1. Вызов [IMAPISession::GetStatusTable,](imapisession-getstatustable.md) чтобы получить доступ к таблице состояния. 
    
2. Создайте ограничение с помощью структуры [SPropertyRestriction,](spropertyrestriction.md) чтобы соответствовать столбце **PR_PROVIDER_DLL_NAME** [(PidTagProviderDllName)](pidtagproviderdllname-canonical-property.md)с именем указанного поставщика. 
    
3. Вызов [IMAPITable::FindRow,](imapitable-findrow.md) чтобы найти строку поставщика. Удостоверение поставщика будет храниться в  столбце PR_IDENTITY_ENTRYID, если оно существует. 
    
 **Извлечение основного удостоверения для сеанса**
  
- Вызов [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **Идентификатор сеанса QueryIdentity** использует значение STATUS_PRIMARY_IDENTITY в столбце **PR_RESOURCE_FLAGS** для одной из строк в таблице состояния. Если ни одна из строк состояния не имеет этого значения, **объект QueryIdentity** назначает удостоверение первому поставщику услуг, который задает три PR_IDENTITY свойств. Если поставщик услуг не поставляет удостоверение, **объект QueryIdentity** возвращает MAPI_W_NO_SERVICE. В этом случае следует создать строку символов для представления общего пользователя, который может служить основным удостоверением. 
    
 **Явный набор основного удостоверения для сеанса**
  
- Call [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md). **Передай MAPIUID для** целевого поставщика услуг. 
    

