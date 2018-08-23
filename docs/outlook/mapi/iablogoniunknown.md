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
ms.openlocfilehash: 4421fcde6ccd2f2ac6245927d9d5d63ddc5200af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573518"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Доступ к ресурсам в поставщика адресных книг.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Предоставляемые:  <br/> |Адресной книги входа объектов  <br/> |
|Реализованный:  <br/> |Поставщиками адресных книг  <br/> |
|Вызывается:  <br/> |MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IABLogon  <br/> |
|Тип указателя:  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем Ошибка поставщика адресной книги.  <br/> |
|[Выход из системы](iablogon-logoff.md) <br/> |Запускает процесс выхода из системы.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Открывает контейнер, системы обмена сообщениями пользователя или список рассылки и возвращает указатель на реализацию интерфейса для дальнейшего доступа.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Сравнение двух идентификаторы записей для определения, является ли они ссылаются на тот же объект.  <br/> |
|[Уведомить](iablogon-advise.md) <br/> |Регистрирует вызывающего абонента для получения уведомлений о указанного события, которые влияют на container, системы обмена сообщениями пользователя или список рассылки.  <br/> |
|[Unadvise](iablogon-unadvise.md) <br/> |Запрос уведомления, которые ранее были настроены с помощью вызова метода **уведомлений** .  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Открывает объект состояние поставщика.  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Открывает запись получателя, который содержит данные, хранимые в адресной книге узла.  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Возвращает таблицу одноразовых шаблоны для создания получателей для добавления в список получателей исходящих сообщений.  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Подготовка списка получателей для дальнейшего использования системой обмена сообщениями.  <br/> |
   
## <a name="remarks"></a>Замечания

Общие сведения о методах **IABLogon** интерфейса [Реализации службы поставщика входа в систему](implementing-service-provider-logon.md)см.
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

