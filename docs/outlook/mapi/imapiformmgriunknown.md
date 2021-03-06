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
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413061"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Позволяет пользователям форм получать сведения о серверах форм и активировать их. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Подвергается:  <br/> |Объекты диспетчера форм  <br/> |
|Реализовано в:  <br/> |Поставщики библиотек форм  <br/> |
|Вызывающая сторона:  <br/> |Просмотр форм  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFormMgr  <br/> |
|Тип указателя:  <br/> |LPMAPIFORMMGR  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[LoadForm](imapiformmgr-loadform.md) <br/> |Запускает форму для открытия существующего сообщения.  <br/> |
|[ResolveMessageClass](imapiformmgr-resolvemessageclass.md) <br/> |Устраняет класс сообщений в его форму в контейнере форм и возвращает информационный объект формы для этой формы.  <br/> |
|[ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |Устраняет группу классов сообщений в их формах в контейнере форм и возвращает массив информационных объектов форм для этих форм.  <br/> |
|[CalcFormPropSet](imapiformmgr-calcformpropset.md) <br/> |Возвращает массив свойств, которые использует группа форм.  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |Запускает форму для создания нового сообщения на основе класса сообщений формы.  <br/> |
|[SelectForm](imapiformmgr-selectform.md) <br/> |Представляет диалоговое окно, которое позволяет пользователю выбрать форму, и возвращает объект информации о форме, описывая эту форму.  <br/> |
|[SelectMultipleForms](imapiformmgr-selectmultipleforms.md) <br/> |Представляет диалоговое окно, которое позволяет пользователю выбирать несколько форм и возвращает массив объектов информации о форме, описывая эти формы.  <br/> |
|[SelectFormContainer](imapiformmgr-selectformcontainer.md) <br/> |Представляет диалоговое окно, которое позволяет пользователю выбрать контейнер формы и возвращает интерфейс для выбранного пользователем объекта контейнера.  <br/> |
|[OpenFormContainer](imapiformmgr-openformcontainer.md) <br/> |Открывает интерфейс [IMAPIFormContainer](imapiformcontaineriunknown.md) для определенного контейнера форм.  <br/> |
|[PrepareForm](imapiformmgr-prepareform.md) <br/> |Скачивает форму для открытия.  <br/> |
|[IsInConflict](imapiformmgr-isinconflict.md) <br/> |Определяет, может ли форма обрабатывать собственные конфликты сообщений.  <br/> |
|[GetLastError](imapiformmgr-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, возникной в объекте диспетчера форм.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

