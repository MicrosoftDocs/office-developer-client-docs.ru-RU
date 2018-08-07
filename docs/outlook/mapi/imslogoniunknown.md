---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 42e2633ac6d534be2c75c47b24c1da5ed9771e18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809433"
---
# <a name="imslogon--iunknown"></a>IMSLogon : IUnknown

  
  
**Относится к**: Outlook 
  
Доступ к ресурсам в сообщение хранилища вход в систему.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Предоставляемые:  <br/> |Объекты входа хранилища сообщений  <br/> |
|Реализованный:  <br/> |Поставщики хранилища сообщений  <br/> |
|Вызывается:  <br/> |MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMSLogon  <br/> |
|Тип указателя:  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetLastError](imslogon-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о последней ошибке, возникшей для объекта хранилища сообщений.  <br/> |
|[Выход из системы](imslogon-logoff.md) <br/> |Поставщик хранилища, выходит из системы сообщение.  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |Открывает папку или объект сообщения и возвращает указатель на объект для дальнейшего доступа.  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |Сравнение двух идентификаторы записей для определения, является ли они ссылаются на тот же объект.  <br/> |
|[Уведомить](imslogon-advise.md) <br/> |Регистрирует объект поставщика хранилища сообщений для уведомлений об изменениях в хранилище сообщений.  <br/> |
|[Unadvise](imslogon-unadvise.md) <br/> |Удаляет регистрацию объекта для уведомление об изменениях хранилища сообщений, ранее созданные с помощью вызова метода **IMSLogon::Advise** .  <br/> |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |Открывает объект состояния.  <br/> |
   
## <a name="remarks"></a>Замечания

Объект вход в систему хранения сообщения является частью поставщика хранилища открыть сообщение, непосредственно вызывающий MAPI. Существует однозначного соответствия между объект вход в систему хранилища сообщений, на котором вызовов MAPI и сообщения храниться объект, который метода клиентских приложений. можно рассматривать вход в систему и хранения объектов как один объект, который предоставляет два из них. Создаются два объекта вместе и освобожденное друг с другом.
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

