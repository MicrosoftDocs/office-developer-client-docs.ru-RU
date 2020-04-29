---
title: Получение основного удостоверения и удостоверения поставщика
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
# <a name="retrieving-primary-and-provider-identity"></a>Получение основного удостоверения и удостоверения поставщика

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Поставщики услуг, обычно поставщики адресных книг, предоставляют возможность указать идентификатор, который можно использовать для представления сеанса в различных ситуациях. Идентификатор поставщика описывается в трех свойствах:
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
Эти свойства задаются как идентификатор записи, отображаемое имя и ключ поиска соответствующего объекта Identity, который обычно является пользователем системы обмена сообщениями. Поставщики, которые предоставляют удостоверение, также устанавливают флаг STATUS_PRIMARY_IDENTITY в своем свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
  
В зависимости от ваших потребностей вы можете использовать идентификатор определенного поставщика или основной идентификатор сеанса. Вы также можете использовать удостоверение поставщика для отображения или получения свойств, таких как **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)). **PR_RESOURCE_PATH**, если этот параметр установлен, содержит путь к файлам, используемым или созданным поставщиком. Получите свойство **PR_RESOURCE_PATH** поставщика, предоставляющее Основное удостоверение, когда требуется найти файлы, которые относятся к пользователю сеанса. 
  
 **Получение удостоверения определенного поставщика**
  
1. Call [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для доступа к таблице состояния. 
    
2. Создание ограничения с использованием структуры [спропертирестриктион](spropertyrestriction.md) для сравнения столбца **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) с именем указанного поставщика. 
    
3. Вызов [IMAPITable:: FindRow](imapitable-findrow.md) для обнаружения строки поставщика. Удостоверение поставщика будет храниться в столбце **PR_IDENTITY_ENTRYID** (если он существует). 
    
 **Извлечение основного удостоверения для сеанса**
  
- Call [IMAPISession:: куеридентити](imapisession-queryidentity.md). **Куеридентити** базовые удостоверения сеанса для существования значения STATUS_PRIMARY_IDENTITY в столбце **PR_RESOURCE_FLAGS** для одной из строк в таблице Status. Если ни для одной из строк состояния не задано это значение, **куеридентити** назначает идентификатор первому поставщику услуг, который задает три свойства PR_IDENTITY. Если поставщик услуг не предоставляет удостоверение, **куеридентити** возвращает MAPI_W_NO_SERVICE. В этом случае необходимо создать строку символов для представления универсального пользователя, который может служить в качестве основного удостоверения. 
    
 **Явное задание основного удостоверения для сеанса**
  
- Call [имсгсервицеадмин:: сетпримаридентити](imsgserviceadmin-setprimaryidentity.md). Передайте **мапиуид** для целевого поставщика услуг. 
    

