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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Просмотр иерархии — это компонент пользовательского интерфейса, используемый для отображения таблиц иерархии контейнеров папок и адресных книг. Читатели иерархии могут отображать члены иерархии на разных уровнях, расширяя и совмесив каждый уровень по требованию.
  
Свойство контейнера, **PR_DEPTH** ([PidTagDepth),](pidtagdepth-canonical-property.md)управляет уровнем, на котором отображается элемент иерархии. Для записей, которые представляют контейнеры или папки адресной книги верхнего **уровня,** PR_DEPTH нулевое значение. Значение этого свойства последовательно добавим для записей на последовательном уровне. То есть, когда пользователь выбирает контейнер верхнего уровня для расширения, отображаются все контейнеры с PR_DEPTH 1.  Когда пользователь расширяет один из этих подсайтов,  отображает контейнеры с PR_DEPTH 2 и т. д. 
  
Читатели иерархии поддерживают различные диапазоны глубин. Для просмотра можно ограничиться одним или двумя уровнями или поддерживать несколько уровней, если в качестве приоритета вы можете отобразить широкие иерархии. 
  
Адресная книга предоставляет представление иерархии для контейнеров верхнего уровня в адресной книге. 
  
 **Доступ к таблице иерархии адресной книги**
  
1. Вызовите [IAddrBook::OpenEntry, передав](iaddrbook-openentry.md)идентификатор записи null, чтобы открыть корневой контейнер адресной книги.
    
2. Вызовите метод [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) корневого контейнера, чтобы получить доступ к таблице иерархии адресной книги MAPI. 
    
 **Доступ к таблице иерархии хранения сообщений по умолчанию**
  
1. Вызов [IMAPISession::GetMsgStoresTable для](imapisession-getmsgstorestable.md) доступа к таблице хранения сообщений. 
    
2. Создайте ограничение, используя структуру [SPropertyRestriction,](spropertyrestriction.md) чтобы ограничить таблицу только теми **строками,** свойство PR_DEFAULT_STORE [(PidTagDefaultStore)](pidtagdefaultstore-canonical-property.md)имеет свойство TRUE. 
    
3. Вызовите [IMAPITable::FindRow,](imapitable-findrow.md)передав ему **SPropertyRestriction,** чтобы найти строку, представляющую хранилище сообщений по умолчанию. 
    
4. Вызовите [IMAPISession::OpenEntry](imapisession-openentry.md), передав свойство **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)из строки по умолчанию в хранилище сообщений в таблице хранения сообщений.
    
5. Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) в хранилище сообщений, чтобы получить **свойство PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId).](pidtagipmsubtreeentryid-canonical-property.md)
    
6. Вызовите метод [IMsgStore::OpenEntry](imsgstore-openentry.md) из магазина сообщений, передав свойство **PR_IPM_SUBTREE_ENTRYID,** чтобы открыть корневую папку поддерево IPM в хранилище сообщений. 
    
7. Вызовите метод [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) корневой папки IPM, чтобы получить доступ к таблице иерархии. 
    

