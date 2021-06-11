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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Доступ к ресурсам в поставщике адресных книг.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Подвергается:  <br/> |Объекты логотипа адресной книги  <br/> |
|Реализовано в:  <br/> |Поставщики адресных книг  <br/> |
|Вызывающая сторона:  <br/> |MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IABLogon  <br/> |
|Тип указателя:  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке поставщика адресной книги.  <br/> |
|[Logoff](iablogon-logoff.md) <br/> |Инициирует процесс входа.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Открывает контейнер, пользователя обмена сообщениями или список рассылки и возвращает указатель в реализацию интерфейса, чтобы обеспечить дополнительный доступ.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Сравнивает два идентификатора записи, чтобы определить, относятся ли они к одному объекту.  <br/> |
|[Консультирование](iablogon-advise.md) <br/> |Регистрирует вызываемого пользователя для получения уведомления о указанных событиях, затрагивающих контейнер, пользователя обмена сообщениями или список рассылки.  <br/> |
|[Unadvise](iablogon-unadvise.md) <br/> |Отменяет уведомления, которые ранее были настроены с помощью вызова метода **Advise.**  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Открывает объект состояния поставщика.  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Открывает запись получателя, которая имеет данные, проживающие в поставщике адресной книги хост- адресов.  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Возвращает таблицу разных шаблонов для создания получателей, которые будут добавлены в список получателей исходятго сообщения.  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Подготавливает список получателей для более позднего использования системой обмена сообщениями.  <br/> |
   
## <a name="remarks"></a>Примечания

Общие сведения о методах интерфейса **IABLogon** см. в окну Реализации поставщика [услуг.](implementing-service-provider-logon.md)
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

