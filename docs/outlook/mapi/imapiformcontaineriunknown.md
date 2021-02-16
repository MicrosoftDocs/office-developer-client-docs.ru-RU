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
ms.openlocfilehash: 208af28307a60615ecafda0992881c5df36aa56f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407531"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Управляет формами в библиотеках форм. Этот интерфейс используется для создания библиотек форм для конкретных приложений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Выставим:  <br/> |Объекты контейнеров форм  <br/> |
|Реализовано в:  <br/> |Поставщики библиотеки форм  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFormContainer  <br/> |
|Тип указателя:  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Устанавливает форму в контейнер формы.  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Удаляет определенную форму из контейнера формы.  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Разрешит класс сообщения в форму в контейнере формы и возвращает объект сведений о форме для этой формы.  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Разрешит группу классов сообщений в их формы в контейнере формы и возвращает массив информационных объектов формы для этих форм.  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Возвращает массив свойств, используемых всеми формами, установленными в контейнере формы.  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Возвращает отображаемого имени контейнера формы.  <br/> |
|[GetLastError](imapiformcontainer-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, содержащую](mapierror.md) сведения о предыдущей ошибке, которая произошла в объекте контейнера формы.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

