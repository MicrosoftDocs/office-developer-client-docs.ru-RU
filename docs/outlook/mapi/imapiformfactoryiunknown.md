---
title: IMAPIFormFactory IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342121"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Поддерживает использование настраиваемых форм времени работы в распределенных вычислительных средах. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Выставим:  <br/> |Объекты фабрики форм  <br/> |
|Реализовано в:  <br/> |Серверы форм  <br/> |
|Вызывающая сторона:  <br/> |Просмотр форм  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFormFactory  <br/> |
|Тип указателя:  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Возвращает объект фабрики классов для формы.  <br/> |
|[GetLastError](imapiformfactory-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке объекта фабрики форм.  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Сохраняет открытый сервер форм в памяти.  <br/> |
   
## <a name="remarks"></a>Примечания

Интерфейс **IMAPIFormFactory** основан на интерфейсе [IClassFactory,](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) а объекты, реализуют **IMAPIFormFactory,** также должны наследоваться от **IClassFactory.**
  
 **IMAPIFormFactory** — это интерфейс, который пользователи форм используют для создания новых объектов форм, когда сервер форм поддерживает несколько классов сообщений (то есть несколько типов объектов формы). 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

