---
title: Иаблогон IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fc8615fcd984623ae9c17c45fb7b51a4498a723b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431080"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Доступ к ресурсам в поставщике адресных книг.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Маписпи. h  <br/> |
|Предоставлено:  <br/> |Объекты входа в адресную книгу  <br/> |
|Реализовано в:  <br/> |Поставщики адресных книг  <br/> |
|Вызывающая сторона:  <br/> |MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IABLogon  <br/> |
|Тип указателя:  <br/> |лпаблогон  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке поставщика адресных книг.  <br/> |
|[Logoff](iablogon-logoff.md) <br/> |Инициирует процесс выхода из системы.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Открывает контейнер, пользователя обмена сообщениями или список рассылки и возвращает указатель на реализацию интерфейса для предоставления дальнейших прав доступа.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на один и тот же объект.  <br/> |
|[Рекомендуем](iablogon-advise.md) <br/> |Регистрирует вызывающий абонент для получения уведомления об указанных событиях, влияющих на контейнер, пользователя обмена сообщениями или список рассылки.  <br/> |
|[Unadvise](iablogon-unadvise.md) <br/> |Отменяет уведомления, которые ранее были настроены с помощью вызова метода **advise** .  <br/> |
|[опенстатусентри](iablogon-openstatusentry.md) <br/> |Открывает объект Status поставщика.  <br/> |
|[опентемплатеид](iablogon-opentemplateid.md) <br/> |Открывает запись получателя, которая содержит данные, находящиеся в поставщике адресной книги узла.  <br/> |
|[жетонеоффтабле](iablogon-getoneofftable.md) <br/> |Возвращает таблицу из одноразовых шаблонов для создания получателей, добавляемых в список получателей исходящего сообщения.  <br/> |
|[препаререЦипс](iablogon-preparerecips.md) <br/> |Подготавливает список получателей для последующего использования системой обмена сообщениями.  <br/> |
   
## <a name="remarks"></a>Примечания

Общие сведения о методах интерфейса **иаблогон** можно найти в статье [Реализация входа в систему поставщика услуг](implementing-service-provider-logon.md).
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

