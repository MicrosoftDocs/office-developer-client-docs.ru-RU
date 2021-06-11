---
title: Единое состояние
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425563"
---
# <a name="uninitialized-state"></a>Единое состояние

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Единое состояние — это объекты начальной формы состояния, которые должны быть в момент их создания. Объекты формы инициализируются с данными сообщений, когда клиентская заявка вызывает [метод IPersistMessage::InitNew](ipersistmessage-initnew.md) или [IPersistMessage::Load](ipersistmessage-load.md) на объект формы. В следующей таблице описываются разрешенные переходы из состояния Unitialized. 
  
|**Метод IPersistMessage**|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Загрузи объект формы с данными по умолчанию.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Загрузить объект формы данными из целевого сообщения.  <br/> |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Возвращаем успех или устанавливаем последнюю ошибку и возвращаем E_UNEXPECTED.  <br/> |Uninitialized  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращаем последнюю ошибку.  <br/> |Uninitialized  <br/> |
|Другие [методы IPersistMessage: методы или методы IUnknown](ipersistmessageiunknown.md) из других интерфейсов  <br/> |Установите последнюю ошибку и верни E_UNEXPECTED.  <br/> |Uninitialized  <br/> |
   
## <a name="see-also"></a>См. также



[Нормальное состояние](normal-state.md)
  
[Состояния форм](form-states.md)

