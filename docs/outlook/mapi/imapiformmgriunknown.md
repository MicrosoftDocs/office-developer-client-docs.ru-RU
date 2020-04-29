---
title: Имапиформмгр IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr
api_type:
- COM
ms.assetid: 8cbd1a42-7de6-43e0-8c77-7711773843d5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413061"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Позволяет читателям форм получать сведения о серверах форм и активировать их. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиформ. h  <br/> |
|Предоставлено:  <br/> |Объекты диспетчера форм  <br/> |
|Реализовано в:  <br/> |Поставщики библиотеки форм  <br/> |
|Вызывающая сторона:  <br/> |Средства просмотра форм  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFormMgr  <br/> |
|Тип указателя:  <br/> |лпмапиформмгр  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[лоадформ](imapiformmgr-loadform.md) <br/> |Запускает форму, чтобы открыть существующее сообщение.  <br/> |
|[ресолвемессажекласс](imapiformmgr-resolvemessageclass.md) <br/> |Разрешает класс сообщения в форму в контейнере формы и возвращает объект сведений о форме для этой формы.  <br/> |
|[ресолвемултиплемессажеклассес](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |Разрешает группу классов сообщений в свои формы в контейнере формы и возвращает массив объектов данных формы для этих форм.  <br/> |
|[калкформпропсет](imapiformmgr-calcformpropset.md) <br/> |Возвращает массив свойств, которые использует группа форм.  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |Запускает форму, чтобы создать новое сообщение на основе класса сообщений формы.  <br/> |
|[селектформ](imapiformmgr-selectform.md) <br/> |Отображает диалоговое окно, которое позволяет пользователю выбрать форму и возвращает объект сведений о форме, который описывает эту форму.  <br/> |
|[селектмултиплеформс](imapiformmgr-selectmultipleforms.md) <br/> |Отображает диалоговое окно, позволяющее пользователю выбрать несколько форм и возвратить массив объектов сведений о форме, описывающих эти формы.  <br/> |
|[селектформконтаинер](imapiformmgr-selectformcontainer.md) <br/> |Отображает диалоговое окно, позволяющее пользователю выбрать контейнер формы и возврат интерфейса для объекта контейнера, выбранного пользователем.  <br/> |
|[опенформконтаинер](imapiformmgr-openformcontainer.md) <br/> |Открывает интерфейс [имапиформконтаинер](imapiformcontaineriunknown.md) для определенного контейнера формы.  <br/> |
|[препареформ](imapiformmgr-prepareform.md) <br/> |Загружает форму для открытия.  <br/> |
|[исинконфликт](imapiformmgr-isinconflict.md) <br/> |Определяет, может ли форма обрабатывать свои собственные конфликты сообщений.  <br/> |
|[GetLastError](imapiformmgr-getlasterror.md) <br/> |Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, возникшей в объекте диспетчера форм.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

