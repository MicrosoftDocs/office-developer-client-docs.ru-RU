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
ms.openlocfilehash: da71e9dd5f2fc20bb1daf528f4466ea29507bf06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429826"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поддерживает доступ к адресной книге MAPI и включает такие операции, как отображение общих диалогов; открытие контейнеров, пользователей сообщений и списков рассылки; и выполнение разрешения имен.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Подвергается:  <br/> |Объекты адресной книги  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения, поставщики услуг  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IAddrBook  <br/> |
|Тип указателя:  <br/> |LPADRBOOK  <br/> |
|Модель транзакции:  <br/> |Неописуемый  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |Открывает запись адресной книги и возвращает указатель в интерфейс, который можно использовать для доступа к записи.  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |Сравнивает два идентификатора записей, принадлежащих конкретному поставщику адресной книги, чтобы определить, относятся ли они к одному объекту адресной книги.  <br/> |
|[Консультирование](iaddrbook-advise.md) <br/> |Регистрирует клиента или поставщика услуг для получения уведомлений об изменениях одной или более записей в адресной книге.  <br/> |
|[Unadvise](iaddrbook-unadvise.md) <br/> |Отменяет регистрацию уведомлений, ранее установленную для записи адресной книги.  <br/> |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |Создает идентификатор записи для разового адреса.  <br/> |
|[NewEntry](iaddrbook-newentry.md) <br/> |Добавляет нового получателя в контейнер адресной книги или в список получателей исходя из сообщения.  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |Выполняет разрешение имен, назначая идентификаторы записей получателям в списке получателей.  <br/> |
|[Address](iaddrbook-address.md) <br/> |Отображает диалоговое окно Outlook адресной книги.  <br/> |
|[Сведения](iaddrbook-details.md) <br/> |Отображает диалоговое окно, в которое отображаются сведения о конкретной записи адресной книги.  <br/> |
|**RecipOptions** <br/> | *Не поддерживается или не документируется.*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *Не поддерживается или не документируется.*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |Возвращает идентификатор входа контейнера, назначенного в качестве личной адресной книги (PAB).  <br/> |
|[SetPAB](iaddrbook-setpab.md) <br/> |Назначит определенный контейнер в качестве личной адресной книги (PAB).  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |Возвращает идентификатор записи для начального контейнера адресной книги.  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |Устанавливает указанный контейнер в качестве контейнера адресной книги по умолчанию, который первоначально был доступен.  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |Возвращает упорядоченный список идентификаторов записей контейнеров, которые будут включены в процесс разрешения имен, инициированный методом [ResolveName.](iaddrbook-resolvename.md)  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |Задает новый путь поиска в профиле, который используется для процесса разрешения имен.  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |Подготавливает список получателей для более позднего использования системой обмена сообщениями.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

