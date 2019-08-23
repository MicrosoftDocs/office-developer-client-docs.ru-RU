---
title: Отображение папок в хранилищах сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 457620dd0f805e78d12fc8feba09f8fc8aedc554
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341351"
---
# <a name="exposing-folders-in-message-stores"></a>Отображение папок в хранилищах сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Каждый поставщик услуг хранилища должен предоставить интерфейс [IMAPIFolder](imapifolderimapicontainer.md) верхнего уровня для клиентских приложений. Папка верхнего уровня соответствует всему хранилищу сообщений; она обеспечивает доступ к папкам, которые пользователь видит в качестве содержимого хранилища сообщений. Кроме того, папка верхнего уровня часто используется по умолчанию в качестве папки для входящих IPC сообщений, а также в качестве папки, из которой отправляются отчеты о прочтении письма. Поставщики хранилища сообщений также должны предоставить поддерево IPM — набор папок, используемых для размещения IPM сообщений — для клиентских приложений. 
  
Клиентские приложения могут открывать папку верхнего уровня, вызвав метод[IMsgStore::OpenEntry](imsgstore-openentry.md) со значением 0 и NULL для параметров_cbEntryId_ и _lpEntryId_ соответственно. Тем не менее, в большинстве случаев, клиентские приложения открывают набор папок, который содержит IPM сообщения. 
  
Для получения списка папок в дереве папок IPM хранилища сообщений, выполните следующее:
  
1. С помощью сессии выполните вызов метода MAPI [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). 
    
2. Используйте указатель полученной базы данных сообщений для вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) для свойства **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
3. Вызовите метод[IMsgStore::OpenEntry](imsgstore-openentry.md) с идентификатором записи, чтобы получить указатель **IMAPIFolder**. 
    
4. Вызовите метод [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) для получения таблицы содержимого папки. 
    
5. Вызовите метод [IMAPITable::QueryRows](imapitable-queryrows.md) для получения списка папок в папке верхнего уровня. 
    
Клиенты MAPI используют эти папки для доступа к прочим объектам папки и объектам сообщений из хранилища сообщений. **IMAPIFolder**и его родительский интерфейс [IMAPIContainer](imapicontainerimapiprop.md), содержат методы, которые ваш поставщик услуг хранилища сообщений должен использовать для заполнения папки объектами сообщения и ответа на запросы клиента для выполнения операций с сообщениями.
  
## <a name="see-also"></a>См. также



[Реализация папок в хранилищах сообщений](implementing-folders-in-message-stores.md)

