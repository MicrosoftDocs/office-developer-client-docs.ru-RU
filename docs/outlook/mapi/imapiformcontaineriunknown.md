---
title: IMAPIFormContainer IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 39f255a277403073132dfd3cd21c995eefe904c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808908"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**Относится к**: Outlook 
  
Управление формами в библиотеках форм. Этот интерфейс используется для создания библиотеки форм конкретного приложения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Предоставляемые:  <br/> |Объекты контейнера формы  <br/> |
|Реализованный:  <br/> |Поставщики библиотеки форм  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFormContainer  <br/> |
|Тип указателя:  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Устанавливает формы в контейнер формы.  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Удаление определенной формы из контейнера формы.  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Разрешает класс сообщения в его формы в контейнере формы и возвращает объект сведения формы для этой формы.  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Разрешает группу классов сообщений в формах в контейнере формы и возвращает массив формы объекты для этих форм.  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Возвращает массив свойств, используемых все формы, установленные в контейнере формы.  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Возвращает отображаемое имя контейнера формы.  <br/> |
|[GetLastError](imapiformcontainer-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , содержащую сведения об ошибке предыдущей появление объект контейнера формы.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

