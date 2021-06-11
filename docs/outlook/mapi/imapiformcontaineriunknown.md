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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Управляет формами в библиотеках форм. Этот интерфейс используется для создания библиотек форм, определенных приложениям. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Подвергается:  <br/> |Объекты контейнера форм  <br/> |
|Реализовано в:  <br/> |Поставщики библиотек форм  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFormContainer  <br/> |
|Тип указателя:  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Устанавливает форму в контейнер формы.  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Удаляет определенную форму из контейнера формы.  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Устраняет класс сообщения в его форму в контейнере формы и возвращает информационный объект формы для этой формы.  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Устраняет группу классов сообщений в их формах в контейнере форм и возвращает массив информационных объектов форм для этих форм.  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Возвращает массив свойств, используемых всеми формами, установленными в контейнере форм.  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Возвращает имя отображения контейнера формы.  <br/> |
|[GetLastError](imapiformcontainer-getlasterror.md) <br/> |Возвращает в объект контейнера формы структуру [MAPIERROR,](mapierror.md) содержащую сведения о предыдущей ошибке.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

