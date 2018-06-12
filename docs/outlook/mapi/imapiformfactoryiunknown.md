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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 651ef6a7c1af70c75a85e13414c4fd7632d30290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808923"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory: IUnknown

  
  
**Применимо к**: Outlook 
  
Поддерживает использование настраиваемых форм во время выполнения в распределенных средах сетей. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Предоставляемые:  <br/> |Объекты фабрики формы  <br/> |
|Реализованный:  <br/> |Серверы формы  <br/> |
|Вызывается:  <br/> |Средства просмотра формы  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFormFactory  <br/> |
|Тип указателя:  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Возвращает объект фабрики класса для формы.  <br/> |
|[GetLastError](imapiformfactory-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущей появление объекта фабрики формы.  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Сохраняет это сервер открытой формы в памяти.  <br/> |
   
## <a name="remarks"></a>Замечания

Интерфейс **IMAPIFormFactory** основано на интерфейс [IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) и объекты, которые реализуют **IMAPIFormFactory** также должен наследовать от **IClassFactory**.
  
 **IMAPIFormFactory** — это интерфейс, который средства просмотра формы используется для создания новых объектов формы, если сервер формы поддерживает несколько классов сообщений (то есть несколько учетных записей введите объекта формы). 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

