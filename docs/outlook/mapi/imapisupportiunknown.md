---
title: IMAPISupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport
api_type:
- COM
ms.assetid: 92bfe604-18dd-46a1-9ae8-0b04167606bd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7daa8ec536a81abc196bbb23a0e1a48e826579e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809191"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**Относится к**: Outlook 
  
Предоставляет реализацию для задач, которые обычно выполняют поставщиков услуг и функции точки входа службы сообщений. Поставщики услуг получать указатель их поддержка объект, когда MAPI вызывает метод их объект поставщика входа в систему. Службы сообщений получают их поддержка указателя на объект в вызове функции их точки входа.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Предоставляемые:  <br/> |Объекты поддержки  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPISup  <br/> |
|Тип указателя:  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetLastError](imapisupport-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , содержащий сведения об ошибке предыдущей объект поддержки.  <br/> |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |Получает адреса MAPI памяти выделение и освобождение функции ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md)).  <br/> |
|[Subscribe](imapisupport-subscribe.md) <br/> |Регистрирует приемника уведомления для получения уведомлений через MAPI.  <br/> |
|[Unsubscribe](imapisupport-unsubscribe.md) <br/> |Отменяет ответственность за отправки уведомлений, которое ранее было установлено с помощью вызова метода **подписаться** .  <br/> |
|[Уведомления](imapisupport-notify.md) <br/> |Отправляет уведомление об указанном события источника уведомлений, изначально зарегистрированных для уведомления с помощью метода **подписки на** .  <br/> |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |Изменяет состояние таблицы путем добавления строки или изменение существующей строки.  <br/> |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |Откроется раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшей access  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |Регистрация поставщика транспорта препроцессору функция (функция, которая соответствует прототип [PreprocessMessage](preprocessmessage.md) ).  <br/> |
|[NewUID](imapisupport-newuid.md) <br/> |Создает новую структуру [MAPIUID](mapiuid.md) для использования в качестве уникального идентификатора.  <br/> |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |Помечает объект недоступным.  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |Передает управление процессора диспетчер очереди MAPI, чтобы он может выполнять любые задачи рассматриваются необходимые.  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |Уведомление об изменении состояния или запрос на обслуживание диспетчер очереди MAPI.  <br/> |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |Создает запись идентификатор указывает адрес.  <br/> |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |Регистрирует **MAPIUID** структуры, который уникальным образом представляет поставщика услуг.  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Сравнение двух идентификаторы записей для определения, является ли они ссылаются на тот же объект.  <br/> |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |Открывает запись получателя в поставщик внешнего адресной книги.  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |Открывает объект и возвращает указатель интерфейса для дальнейшей доступа.  <br/> |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |Возвращает указатель на таблице одноразовых MAPI (список шаблонов, что все в адресной книге поставщиков поддержка создания новых получателей).  <br/> |
|[Адрес](imapisupport-address.md) <br/> |Отображает диалоговое окно Общие адреса.  <br/> |
|[Сведения](imapisupport-details.md) <br/> |Отображает диалоговое окно, которое предоставляет подробные сведения о записи определенного адресной книги.  <br/> |
|[NewEntry](imapisupport-newentry.md) <br/> |Добавляет нового получателя непосредственно к контейнеру адресной книги или списка получателей исходящих сообщений.  <br/> |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |Отображает окно свойств конфигурации.  <br/> |
|[CopyMessages](imapisupport-copymessages.md) <br/> |Копирование или перемещение сообщений из одной папки в другую папку.  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |Копирование или перемещение папки текущей родительской папки в другую.  <br/> |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |Копирование или перемещение всех свойств одного объекта, за исключением специально исключенные свойства на другой объект.  <br/> |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |Копирование или Перемещение одного или нескольких свойств объекта на другой объект.  <br/> |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |Извлекает объект хода выполнения, который отображает индикатор хода выполнения.  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |Создает доступ на чтение или nonread отчет для сообщения.  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |Подготавливает сообщение для отправки диспетчер очереди MAPI.  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |Завершает список получателей сообщения, возможность расширения списков рассылок определенного.  <br/> |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |������������ ������������ ���������.  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |Предоставляет доступ к адресной книге.  <br/> |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |Выполняет постобработку сообщение.  <br/> |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |Запрашивает надлежащей выпуске хранилища сообщений.  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |Создает отчеты о доставке и недоставке.  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |Преобразует идентификатор внутренней записи хранилища сообщений идентификатор записи в стандартный формат MAPI.  <br/> |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |Вносятся изменения в сообщение хранения основного раздела профиля.  <br/> |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |Реализует объект хранилища для доступа к потоку.  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |Создает объект сообщения службы поддержки.  <br/> |
   
## <a name="remarks"></a>Замечания

Адресной книги, хранилищ сообщений, поставщиками транспорта и сообщений, что службы каждого имеют собственные объекты поддержки. Поставщики службы и службы сообщений вызывать методы в их объекты поддержки как часть их реализации других методов интерфейса. Каждый объект поддержки различных имеет завершения реализации методов, которые применяются к вызывающему объекту; метод, не соответствующие возвращает MAPI_E_NO_SUPPORT. Объекты поддержки поставщик адресной книги имеют реализации для следующих методов:
  
||||
|:-----|:-----|:-----|
|**Адрес** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**Сведения** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**GetLastError** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NewEntry** <br/> |**NewUID** <br/> |
|**Уведомления** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**OpenProfileSection** <br/> |**OpenTemplateID** <br/> |**SetProviderUID** <br/> |
|**Subscribe** <br/> |**Unsubscribe** <br/> |**WrapStoreEntryID** <br/> |
   
Объекты поддержки поставщика хранилища сообщений имеют реализации для следующих методов:
  
||||
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**CompleteMsg** <br/> |**CopyFolder** <br/> |
|**CopyMessages** <br/> |**CreateOneOff** <br/> |**DoCopyProps** <br/> |
|**DoCopyTo** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**DoSentMail** <br/> |**ExpandRecips** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**IStorageFromStream** <br/> |**ModifyProfile** <br/> |**ModifyStatusRow** <br/> |
|**NewUID** <br/> |**Уведомления** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**OpenProfileSection** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**SetProviderUID** <br/> |**SpoolerNotify** <br/> |
|**StoreLogoffTransports** <br/> |**Subscribe** <br/> |**Unsubscribe** <br/> |
|**WrapStoreEntryID** <br/> |
   
Объекты поддержки поставщика транспорта имеют реализации для следующих методов:
  
||||
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**GetLastError** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Уведомления** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Subscribe** <br/> |**Unsubscribe** <br/> |
   
Сообщение службы поддержки объекты имеют реализации для следующих методов:
  
|||
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

