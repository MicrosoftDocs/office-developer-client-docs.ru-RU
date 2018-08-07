---
title: IMAPIContainer IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e24f5ebd73a4652876282099f1460762c150b94d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808832"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**Относится к**: Outlook 
  
Управляет высокого уровня операций в контейнере объекты, такие как адресных книг, списков рассылки и папок. [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md), и [IDistList: IMAPIContainer](idistlistimapicontainer.md) интерфейсы являются производными от **IMAPIContainer**.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Папка, контейнер адресной книги и объекты списка рассылки  <br/> |
|Реализованный:  <br/> |Хранение сообщений, адресной книги и поставщиков удаленных транспорта  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIContainer  <br/> |
|Тип указателя:  <br/> |LPMAPICONTAINER  <br/> |
|Модель транзакций:  <br/> |Абстрактный класс, никогда не реализовано  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetContentsTable](imapicontainer-getcontentstable.md) <br/> |Возвращает указатель на таблицу содержимого контейнера.  <br/> |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |Возвращает указатель на таблицу иерархии контейнера.  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Открывает объект в контейнере, возвращает указатель интерфейса для дальнейшей доступа.  <br/> |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |Устанавливает условия поиска для контейнера.  <br/> |
|[GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |Получает параметры поиска для контейнера.  <br/> |
   
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Чтение и запись  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

