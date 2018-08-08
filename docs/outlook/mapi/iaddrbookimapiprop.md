---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0e39f2603a1eef45c456b7fb58744b79c6b75f16
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808761"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**Относится к**: Outlook 
  
Поддерживает доступ к адресной книге MAPI, а также операции, такие как отображение общие диалоговые окна; Открытие контейнеров, системы обмена сообщениями пользователей и списки рассылки; и разрешение имен для выполнения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Предоставляемые:  <br/> |Объекты адресной книги  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения, поставщиков услуг  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IAddrBook  <br/> |
|Тип указателя:  <br/> |LPADRBOOK  <br/> |
|Модель транзакций:  <br/> |Не для записи  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |Открывает запись книги и возвращает указатель на интерфейс, который можно использовать для доступа к операции.  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |Сравнение двух идентификаторы записей, относящихся к конкретной адресной книге, чтобы определить, является ли они ссылаются на один и тот же объект адресной книги.  <br/> |
|[Уведомить](iaddrbook-advise.md) <br/> |Регистрация клиента или поставщика для получения уведомлений об изменениях в одну или несколько записей в адресной книге.  <br/> |
|[Unadvise](iaddrbook-unadvise.md) <br/> |Отмена регистрации уведомлений, ранее созданные записи адресной книги.  <br/> |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |Создает запись идентификатор указывает адрес.  <br/> |
|[NewEntry](iaddrbook-newentry.md) <br/> |Добавляет нового получателя контейнер адресной книги или списка получателей исходящих сообщений.  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |Выполняет разрешение имен, назначение идентификаторов запись для получателей в список получателей.  <br/> |
|[Адрес](iaddrbook-address.md) <br/> |Отображает диалоговое окно Outlook адресной книги.  <br/> |
|[Сведения](iaddrbook-details.md) <br/> |Отображает диалоговое окно, которое предоставляет подробные сведения о записи определенного адресной книги.  <br/> |
|**RecipOptions** <br/> | *Не поддерживается, документированных.*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *Не поддерживается, документированных.*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |Возвращает идентификатор записи контейнера, который используется в качестве Личная адресная книга (адресной книги).  <br/> |
|[SetPAB](iaddrbook-setpab.md) <br/> |Назначает конкретным контейнером Личная адресная книга (адресной книги).  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |Возвращает идентификатор записи для контейнер начальной адресной книги.  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |Устанавливает указанный контейнер как контейнер адресной книги по умолчанию, который изначально становятся доступными.  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |Возвращает упорядоченный список идентификаторов запись контейнеров, которые будут включены в процесс разрешения имен, инициированных метод [ResolveName](iaddrbook-resolvename.md) .  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |Задает новый путь для поиска профиля, который используется для процесса разрешения имен.  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |Подготовка списка получателей для дальнейшего использования системой обмена сообщениями.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

