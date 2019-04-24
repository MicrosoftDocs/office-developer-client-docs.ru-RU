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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348834"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Доступ к ресурсам в поставщике адресных книг.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Маписпи. h  <br/> |
|Предоставлено:  <br/> |Объекты входа в адресную книгу  <br/> |
|Реализовано в:  <br/> |Поставщики адресных книг  <br/> |
|Вызывающая сторона:  <br/> |MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_иаблогон  <br/> |
|Тип указателя:  <br/> |ЛПАБЛОГОН  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке поставщика адресных книг.  <br/> |
|[Logoff](iablogon-logoff.md) <br/> |Инициирует процесс выхода из системы.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Открывает контейнер, пользователя обмена сообщениями или список рассылки и возвращает указатель на реализацию интерфейса для предоставления дальнейших прав доступа.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на один и тот же объект.  <br/> |
|[Рекомендуем](iablogon-advise.md) <br/> |Регистрирует вызывающий абонент для получения уведомления об указанных событиях, влияющих на контейнер, пользователя обмена сообщениями или список рассылки.  <br/> |
|[Unadvise](iablogon-unadvise.md) <br/> |ОтМеняет уведомления, которые ранее были настроены с помощью вызова метода **advise** .  <br/> |
|[Опенстатусентри](iablogon-openstatusentry.md) <br/> |Открывает объект Status поставщика.  <br/> |
|[Опентемплатеид](iablogon-opentemplateid.md) <br/> |Открывает запись получателя, которая содержит данные, находящиеся в поставщике адресной книги узла.  <br/> |
|[Жетонеоффтабле](iablogon-getoneofftable.md) <br/> |Возвращает таблицу из одноразовых шаблонов для создания получателей, добавляемых в список получателей исходящего сообщения.  <br/> |
|[ПрепаререЦипс](iablogon-preparerecips.md) <br/> |ПодГотавливает список получателей для последующего использования системой обмена сообщениями.  <br/> |
   
## <a name="remarks"></a>Примечания

Общие сведения о методах интерфейса **иаблогон** можно найти в статье [Реализация входа в систему поставщика услуг](implementing-service-provider-logon.md).
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

