---
title: Написание просмотра иерархии
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421132"
---
# <a name="writing-a-hierarchy-viewer"></a>Написание просмотра иерархии

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Зритель иерархии — это компонент пользовательского интерфейса, используемый для отображения таблиц иерархии контейнеров папок и адресных книг. Зрители иерархии могут отображать членов иерархии на разных уровнях, расширяя и заключая контракты на каждом уровне по запросу.
  
Свойство контейнера **PR_DEPTH** [(PidTagDepth)](pidtagdepth-canonical-property.md)контролирует уровень отображения члена иерархии. Записи, которые представляют контейнеры или папки с адресной книгой **верхнего уровня,** имеют свойство PR_DEPTH к нулю. Значение этого свойства последовательно приумножено для записей на последовательном уровне. То есть, когда пользователь выбирает для расширения контейнер верхнего уровня, отобразить все контейнеры с PR_DEPTH 1.  Когда пользователь расширяет один из этих субконтейнов,  отобразить контейнеры с PR_DEPTH 2 и т. д. 
  
Зрители иерархии поддерживают различные диапазоны глубин. Можно ограничить просмотр только одним или двумя уровнями или поддерживать несколько уровней, если приоритет отобразить экспансивную иерархию. 
  
Адресная книга предоставляет зрителю иерархию для контейнеров верхнего уровня в адресной книге. 
  
 **Доступ к таблице иерархии адресных книг**
  
1. Вызов [IAddrBook::OpenEntry,](iaddrbook-openentry.md)передав идентификатор записи null, чтобы открыть корневой контейнер адресной книги.
    
2. Вызов метода [IMAPIContainer корневого контейнера::GetHierarchyTable,](imapicontainer-gethierarchytable.md) чтобы получить доступ к таблице иерархии адресной книги MAPI. 
    
 **Доступ к таблице иерархии магазина сообщений по умолчанию**
  
1. Вызов [IMAPISession::GetMsgStoresTable,](imapisession-getmsgstorestable.md) чтобы получить доступ к таблице хранения сообщений. 
    
2. Создайте ограничение с помощью [структуры SPropertyRestriction,](spropertyrestriction.md) чтобы ограничить таблицу только теми строками, которые имеют **свойство PR_DEFAULT_STORE** [(PidTagDefaultStore)](pidtagdefaultstore-canonical-property.md)для true. 
    
3. Вызов [IMAPITable::FindRow](imapitable-findrow.md), передав его **SPropertyRestriction**, чтобы найти строку, представляющую хранилище сообщений по умолчанию. 
    
4. Вызов [IMAPISession::OpenEntry](imapisession-openentry.md), передача свойства **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)из строки магазина сообщений по умолчанию в таблице хранения сообщений.
    
5. Для получения свойства[PR_IPM_SUBTREE_ENTRYID (PidTagIpmSubtreeEntryId)](pidtagipmsubtreeentryid-canonical-property.md)вызываем метод [IMAPIProp::GetProps](imapiprop-getprops.md) в хранилище сообщений. 
    
6. Вызов метода [IMsgStore::OpenEntry](imsgstore-openentry.md) магазина сообщений, **передав** свойство PR_IPM_SUBTREE_ENTRYID, чтобы открыть корневую папку подтриба IPM магазина сообщений. 
    
7. Вызов метода IPM корневой папки [IMAPIContainer::GetHierarchyTable,](imapicontainer-gethierarchytable.md) чтобы получить доступ к таблице иерархии. 
    

