---
title: IMAPIFormMgr IUnknown
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
ms.openlocfilehash: 4fdd50a1108a6546445516664b01fb0f994fbfdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808951"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr : IUnknown

  
  
**Относится к**: Outlook 
  
Включение средств просмотра формы для получения информации о и активации серверов формы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Предоставляемые:  <br/> |Объекты диспетчер форм  <br/> |
|Реализованный:  <br/> |Поставщики библиотеки форм  <br/> |
|Вызывается:  <br/> |Средства просмотра формы  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFormMgr  <br/> |
|Тип указателя:  <br/> |LPMAPIFORMMGR  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[LoadForm](imapiformmgr-loadform.md) <br/> |Запускает существующее сообщение при открытии формы.  <br/> |
|[ResolveMessageClass](imapiformmgr-resolvemessageclass.md) <br/> |Разрешает класс сообщения в его формы в контейнере формы и возвращает объект сведения формы для этой формы.  <br/> |
|[ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |Разрешает группу классов сообщений в формах в контейнере формы и возвращает массив формы объекты для этих форм.  <br/> |
|[CalcFormPropSet](imapiformmgr-calcformpropset.md) <br/> |Возвращает массив свойств, которые использует группа форм.  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |Открывает форму для создания нового сообщения на основе класса сообщения формы.  <br/> |
|[SelectForm](imapiformmgr-selectform.md) <br/> |Предоставляет диалоговое окно, которое позволяет пользователю выбрать форму и возвращает объект данные формы с описанием данной форме.  <br/> |
|[SelectMultipleForms](imapiformmgr-selectmultipleforms.md) <br/> |Предоставляет диалоговое окно, которое позволяет пользователю выбрать нескольких форм и возвращает массив формы объекты, которые описывают формах.  <br/> |
|[SelectFormContainer](imapiformmgr-selectformcontainer.md) <br/> |Отображает диалоговое окно, которое позволяет пользователю выбрать контейнер, формы и возвращает интерфейс для объекта контейнера выбранный пользователем.  <br/> |
|[OpenFormContainer](imapiformmgr-openformcontainer.md) <br/> |Откроется интерфейс [IMAPIFormContainer](imapiformcontaineriunknown.md) для контейнера конкретной формы.  <br/> |
|[PrepareForm](imapiformmgr-prepareform.md) <br/> |Файлы для загрузки для открытия формы.  <br/> |
|[IsInConflict](imapiformmgr-isinconflict.md) <br/> |Определяет ли формы можно обработать собственный конфликтов сообщения.  <br/> |
|[GetLastError](imapiformmgr-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , содержащий сведения об ошибке предыдущей появление объект диспетчер форм.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

