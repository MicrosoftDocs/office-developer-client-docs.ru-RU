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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286722"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Управляет операциями высокого уровня для объектов контейнеров, таких как адресные книги, списки рассылки и папки. Интерфейсы [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [иабконтаинер: IMAPIContainer](iabcontainerimapicontainer.md)и [идистлист: IMAPIContainer](idistlistimapicontainer.md) являются производными от **IMAPIContainer**.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Предоставлено:  <br/> |Папка, контейнер адресной книги и объекты списка рассылки  <br/> |
|Реализовано в:  <br/> |Хранилище сообщений, адресные книги и удаленные поставщики транспорта  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_имапиконтаинер  <br/> |
|Тип указателя:  <br/> |ЛПМАПИКОНТАИНЕР  <br/> |
|Модель транзакции:  <br/> |Абстрактный класс, никогда не реализован  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[Жетконтентстабле](imapicontainer-getcontentstable.md) <br/> |Возвращает указатель на таблицу содержимого контейнера.  <br/> |
|[Жесиерарчитабле](imapicontainer-gethierarchytable.md) <br/> |Возвращает указатель на таблицу иерархии контейнера.  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Открывает объект в контейнере, возвращая указатель интерфейса для дальнейшего доступа.  <br/> |
|[Сетсеарчкритериа](imapicontainer-setsearchcriteria.md) <br/> |Устанавливает критерии поиска для контейнера.  <br/> |
|[Жетсеарчкритериа](imapicontainer-getsearchcriteria.md) <br/> |Получает условия поиска для контейнера.  <br/> |
   
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**Пр_контаинер_хиерарчи** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_контаинер_контентс** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_контаинер_флагс** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Чтение и запись  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

