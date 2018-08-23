---
title: Написание средства просмотра иерархии
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6ff394c95dfa3166d39dcba4b0c577dcfac7b8d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581596"
---
# <a name="writing-a-hierarchy-viewer"></a>Написание средства просмотра иерархии

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Просмотр иерархии — компонент пользовательского интерфейса, который используется для отображения папки и адресной книги контейнер таблиц иерархии. Средства просмотра иерархии может отображать элементы иерархии на разных уровнях, развертывание и контракт каждого уровня по запросу.
  
Свойство контейнера, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) определяет уровень отображения элемент иерархии. Элементы, соответствующие контейнеры верхнего уровня адресной книги или папки, имеют свойство **PR_DEPTH** равным нулю. Значение этого свойства последовательно увеличивается для записи в последовательный уровни. То есть когда пользователь выбирает верхнего уровня контейнер, чтобы развернуть, отображение всех контейнеров с **PR_DEPTH** значение 1. Когда пользователь раскрывает один из этих субконтейнеров, отображение контейнеров с набором **PR_DEPTH** 2 и так далее. 
  
Средства просмотра иерархии поддерживают различные диапазон глубины. Можно ограничить используемого средства просмотра для уровней только один или два или если отображение обширный иерархии приоритет может поддерживать несколько уровней. 
  
В адресной книге предоставляет средство просмотра иерархии для контейнеров верхнего уровня в адресной книге. 
  
 **Для доступа к таблице иерархии адресной книги**
  
1. Вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md), передав идентификатор значение null, запись, чтобы открыть корневой контейнер адресной книги.
    
2. Вызов метода [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) корневой контейнер для доступа к таблице иерархии адресной книги MAPI. 
    
 **Для доступа к таблице иерархии хранилища сообщений по умолчанию**
  
1. Вызов [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) для доступа к таблице хранилища сообщений. 
    
2. Выполните построение ограничение с помощью структуры [SPropertyRestriction](spropertyrestriction.md) для ограничения в таблице, чтобы только строки, **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) свойство должно быть указано значение TRUE. 
    
3. Вызовите [IMAPITable::FindRow](imapitable-findrow.md), передав ее **SPropertyRestriction**, чтобы найти строки, представляющие хранилище сообщений по умолчанию. 
    
4. Вызовите [IMAPISession::OpenEntry](imapisession-openentry.md), передав в свойстве **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) из хранилища сообщений по умолчанию строку в таблице хранилища сообщений.
    
5. Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) хранилище сообщений для получения свойства **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
6. Вызовите метод [IMsgStore::OpenEntry](imsgstore-openentry.md) хранилища сообщений, передав свойство **PR_IPM_SUBTREE_ENTRYID** , чтобы открыть корневую папку поддерева IPM хранилища сообщений. 
    
7. Вызов метода [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) IPM корневую папку для доступа к его таблицы иерархии. 
    

