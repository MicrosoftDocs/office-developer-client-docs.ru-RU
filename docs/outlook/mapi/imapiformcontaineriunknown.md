---
title: Имапиформконтаинер IUnknown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342191"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Управляет формами в библиотеках форм. Этот интерфейс используется для создания библиотек форм, характерных для приложений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиформ. h  <br/> |
|Предоставлено:  <br/> |Объекты контейнера формы  <br/> |
|Реализовано в:  <br/> |Поставщики библиотеки форм  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_имапиформконтаинер  <br/> |
|Тип указателя:  <br/> |ЛПМАПИФОРМКОНТАИНЕР  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[Инсталлформ](imapiformcontainer-installform.md) <br/> |Устанавливает форму в контейнер форм.  <br/> |
|[Ремовеформ](imapiformcontainer-removeform.md) <br/> |Удаляет определенную форму из контейнера формы.  <br/> |
|[Ресолвемессажекласс](imapiformcontainer-resolvemessageclass.md) <br/> |Разрешает класс сообщения в форму в контейнере формы и возвращает объект сведений о форме для этой формы.  <br/> |
|[Ресолвемултиплемессажеклассес](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Разрешает группу классов сообщений в свои формы в контейнере формы и возвращает массив объектов данных формы для этих форм.  <br/> |
|[Калкформпропсет](imapiformcontainer-calcformpropset.md) <br/> |Возвращает массив свойств, используемых всеми формами, установленными в контейнере форм.  <br/> |
|[Вывод на экран](imapiformcontainer-getdisplay.md) <br/> |Возвращает отображаемое имя контейнера формы.  <br/> |
|[GetLastError](imapiformcontainer-getlasterror.md) <br/> |Возвращает структуру [мапиеррор](mapierror.md) , содержащую сведения о предыдущей ошибке, возникшей в объекте контейнера формы.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

