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
ms.openlocfilehash: 8be3b1857d539f81e42d2ac3e5813afa73513a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406124"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Управление высокоуровневой операцией на контейнерных объектах, таких как адресные книги, списки рассылки и папки. ИнтерфейсЫ [IMAPIFolder : IMAPIContainer,](imapifolderimapicontainer.md) [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)и [IDistList: интерфейсы IMAPIContainer](idistlistimapicontainer.md) получены из **интерфейсов IMAPIContainer**.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Подвергается:  <br/> |Папка, контейнер адресной книги и объекты списка рассылки  <br/> |
|Реализовано в:  <br/> |Хранилище сообщений, адресная книга и поставщики удаленных транспортных средств  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIContainer  <br/> |
|Тип указателя:  <br/> |LPMAPICONTAINER  <br/> |
|Модель транзакции:  <br/> |Абстрактный класс, никогда не реализованный  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[GetContentsTable](imapicontainer-getcontentstable.md) <br/> |Возвращает указатель в таблицу содержимого контейнера.  <br/> |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |Возвращает указатель в таблицу иерархии контейнера.  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Открывает объект в контейнере, возвращая указатель интерфейса для дальнейшего доступа.  <br/> |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |Устанавливает критерии поиска для контейнера.  <br/> |
|[GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |Получает критерии поиска для контейнера.  <br/> |
   
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_CONTAINER_FLAGS** [(PidTagContainerFlags)](pidtagcontainerflags-canonical-property.md)  <br/> |Чтение и запись  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

