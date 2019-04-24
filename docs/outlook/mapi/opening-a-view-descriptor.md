---
title: Открытие дескриптора представления
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ce53e5a91f6fa340728872457eae7f6514e287aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326210"
---
# <a name="opening-a-view-descriptor"></a>Открытие дескриптора представления
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Многие папки можно открыть с обычным представлением, представлением по умолчанию или любым количеством настраиваемых представлений. В этом представлении показано, как отобразить содержимое папки. Обычное представление используется при отсутствии альтернативного представления и при первом открытии папки. Если альтернативное представление существует, его необходимо использовать для открытия папки.
  
Представление описывается в сообщении, называемом дескриптором представления. Дескрипторы представлений обычно создаются как связанные сообщения и могут отображаться в папках "Общие" или "личное представление" или в любой папке IPM.
  
### <a name="to-open-a-view-descriptor"></a>Открытие дескриптора представления
  
1. Call [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md) , чтобы получить связанную таблицу содержимого для папки. 
    
2. Создайте ограничение, которое будет искать только сообщения с классом сообщений, зарезервированным для дескрипторов просмотра и вызовов [IMAPITable:: restrict](imapitable-restrict.md) to Limit для таблицы и [IMAPITable:: QueryRows](imapitable-queryrows.md) для получения соответствующих строк или...
    
   ВыЗовите метод [IMAPIProp::](imapiprop-getprops.md) -PROPS папки, чтобы получить свойство **пр_дефаулт_виев_ентрид** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)). **Пр_дефаулт_виев_ентрид** содержит идентификатор записи для сообщения, содержащего дескриптор представления по умолчанию для папки. Этот вызов будет успешным, если папка поддерживает использование флага МАПИ_АССОЦИАТЕД при вызовах [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) и [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md).
    
3. Call [IMsgStore:: OpenEntry](imsgstore-openentry.md) с идентификатором элемента дескриптора представления, чтобы открыть его. 
    

