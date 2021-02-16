---
title: IABLogon IUnknown
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
  
Доступ к ресурсам в поставщике адресной книги.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Выставим:  <br/> |Объекты для логотипа адресной книги  <br/> |
|Реализовано в:  <br/> |Поставщики адресных книг  <br/> |
|Вызывающая сторона:  <br/> |MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IABLogon  <br/> |
|Тип указателя:  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке поставщика адресной книги.  <br/> |
|[Logoff](iablogon-logoff.md) <br/> |Инициирует процесс выйдите из нее.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Открывает контейнер, пользователя обмена сообщениями или список рассылки и возвращает указатель на реализацию интерфейса для обеспечения дальнейшего доступа.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Сравнивает два идентификатора записей, чтобы определить, относятся ли они к одному объекту.  <br/> |
|[Консультация](iablogon-advise.md) <br/> |Регистрирует вызываемого пользователя для получения уведомлений об указанных событиях, влияющих на контейнер, пользователя обмена сообщениями или список рассылки.  <br/> |
|[Unadvise](iablogon-unadvise.md) <br/> |Отменяет уведомления, которые ранее были настроены с помощью вызова метода **Advise.**  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Открывает объект состояния поставщика.  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Открывает запись получателя с данными, которые есть в поставщике адресной книги хост-адреса.  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Возвращает таблицу разных шаблонов для создания получателей, добавляемой в список получателей исходяного сообщения.  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Подготавливает список получателей к дальнейшему использованию системой обмена сообщениями.  <br/> |
   
## <a name="remarks"></a>Примечания

Общие сведения о методах интерфейса **IABLogon** см. в этой [теме.](implementing-service-provider-logon.md)
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

