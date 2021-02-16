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
ms.openlocfilehash: 6da488408d3be9464d6ae1e016d5095707d451e4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415441"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет реализации задач, которые обычно выполняются поставщиками служб и функциями точеки входа службы сообщений. Поставщики услуг получают указатель на свой объект поддержки, когда MAPI вызывает метод для их объекта поставщика. Службы сообщений получают указатель объекта поддержки при вызове функции точки входа.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Выставим:  <br/> |Объекты поддержки  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPISup  <br/> |
|Тип указателя:  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[GetLastError](imapisupport-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке объекта поддержки.  <br/> |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |Извлекает адреса функций выделения памяти и распределения MAPI ([MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer).](mapifreebuffer.md)  <br/> |
|[Subscribe](imapisupport-subscribe.md) <br/> |Регистрирует приемник уведомлений для получения уведомлений через MAPI.  <br/> |
|[Отмена подписки](imapisupport-unsubscribe.md) <br/> |Отменяет ответственность за отправку уведомлений, которые ранее были установлены с помощью вызова метода **Subscribe.**  <br/> |
|[Уведомления](imapisupport-notify.md) <br/> |Отправляет уведомление об указанном событии источнику консультаций, который изначально зарегистрировался для уведомления с помощью метода **Subscribe.**  <br/> |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |Изменяет таблицу состояния, добавляя новую строку или изменяя существующую строку.  <br/> |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |Открывает раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |Регистрирует функцию препроцессора поставщика транспорта (функцию, которая соответствует прототипу [PreprocessMessage).](preprocessmessage.md)  <br/> |
|[NewUID](imapisupport-newuid.md) <br/> |Создает новую структуру [MAPIUID,](mapiuid.md) которая будет использоваться в качестве уникального идентификатора.  <br/> |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |Пометка объекта как непригодного для 2013 г.  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |Предоставляет управление ЦП для пула MAPI, чтобы он выполнял любые задачи, которые он считает необходимыми.  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |Сообщает пулу MAPI об изменении состояния или запросе на обслуживание.  <br/> |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |Создает идентификатор записи для разовый адрес.  <br/> |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |Регистрирует **структуру MAPIUID,** которая однозначно представляет поставщика услуг.  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Сравнивает два идентификатора записей, чтобы определить, относятся ли они к одному объекту.  <br/> |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |Открывает запись получателя во внешнем поставщике адресной книги.  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |Открывает объект и возвращает указатель интерфейса для дальнейшего доступа.  <br/> |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |Возвращает указатель на односервную таблицу MAPI (список шаблонов, поддерживаемый всеми поставщиками адресных книг для создания новых получателей).  <br/> |
|[Address](imapisupport-address.md) <br/> |Отображает диалоговое окно общего адреса.  <br/> |
|[Details](imapisupport-details.md) <br/> |Отображает диалоговое окно с подробными сведениями об определенной записи адресной книги.  <br/> |
|[NewEntry](imapisupport-newentry.md) <br/> |Добавляет нового получателя непосредственно в контейнер адресной книги или в список получателей исходяного сообщения.  <br/> |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |Отображает таблицу свойств конфигурации.  <br/> |
|[CopyMessages](imapisupport-copymessages.md) <br/> |Копирует или перемещает сообщения из одной папки в другую.  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |Копирует или перемещает папку из текущей родительской папки в другую родительную папку.  <br/> |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |Копирует или перемещает все свойства одного объекта, кроме специально исключенных, в другой объект.  <br/> |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |Копирует или перемещает одно или несколько свойств объекта в другой объект.  <br/> |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |Извлекает объект хода выполнения, который отображает индикатор хода выполнения.  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |Создает отчет о прочтях или непрочитанных сообщениях.  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |Подготовка сообщения для отправки в пул MAPI.  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |Завершает список получателей сообщения, расширяя определенные списки рассылки.  <br/> |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |������������ ������������ ���������.  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |Предоставляет доступ к адресной книге.  <br/> |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |Выполняет постобсказку сообщения.  <br/> |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |Запрашивает упорядоченный выпуск хранения сообщений.  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |Создает отчеты о доставке и ненастройстве.  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |Преобразует внутренний идентификатор записи в хранилище сообщений в идентификатор записи в стандартном формате MAPI.  <br/> |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |Вносит изменения в раздел профиля хранения сообщений без изменений.  <br/> |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |Реализует объект хранилища для доступа к потоку.  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |Создает объект поддержки службы сообщений.  <br/> |
   
## <a name="remarks"></a>Примечания

Адресные книги, хранилища сообщений, поставщики транспорта и службы сообщений имеют собственные объекты поддержки. Поставщики услуг и службы сообщений звонят методам в своих объектах поддержки в рамках реализации других методов интерфейса. Каждый объект поддержки имеет полные реализации методов, которые применяются к вызываемой стороне; методы, которые не применимы к возврату MAPI_E_NO_SUPPORT. Объекты поддержки поставщиков адресных книг имеют реализации для следующих методов:
  
||||
|:-----|:-----|:-----|
|**Address** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**Details** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**GetLastError** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NewEntry** <br/> |**NewUID** <br/> |
|**Уведомления** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**OpenProfileSection** <br/> |**OpenTemplateID** <br/> |**SetProviderUID** <br/> |
|**Subscribe** <br/> |**Отмена подписки** <br/> |**WrapStoreEntryID** <br/> |
   
Объекты поддержки поставщика store сообщений имеют реализации для следующих методов:
  
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
|**StoreLogoffTransports** <br/> |**Subscribe** <br/> |**Отмена подписки** <br/> |
|**WrapStoreEntryID** <br/> |
   
Объекты поддержки поставщиков транспорта имеют реализации для следующих методов:
  
||||
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**GetLastError** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Уведомления** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Subscribe** <br/> |**Отмена подписки** <br/> |
   
Объекты поддержки службы сообщений имеют реализации для следующих методов:
  
|||
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

