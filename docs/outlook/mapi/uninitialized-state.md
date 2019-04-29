---
title: Неинициализированное состояние
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
# <a name="uninitialized-state"></a>Неинициализированное состояние

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Неинициализированное состояние — это начальные объекты формы состояния, которые должны находиться в момент создания. Объекты Form инициализируются данными сообщений, когда клиентское приложение вызывает метод [иперсистмессаже:: инитнев](ipersistmessage-initnew.md) или [Иперсистмессаже:: Load](ipersistmessage-load.md) объекта Form. В следующей таблице описаны допустимые переходы из состояния Унитиализед. 
  
|**Метод Иперсистмессаже**|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Загрузка объекта Form с данными по умолчанию.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Загрузка объекта Form с данными из целевого сообщения.  <br/> |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Возвращает сообщение об успешном выполнении или задает последнюю ошибку и возвращает Е_УНЕКСПЕКТЕД.  <br/> |Неинициализированное  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возврат последней ошибки.  <br/> |Неинициализированное  <br/> |
|Другие [иперсистмессаже:](ipersistmessageiunknown.md) методы или методы IUnknown из других интерфейсов  <br/> |ПриСвойте последней ошибке значение и возвратите Е_УНЕКСПЕКТЕД.  <br/> |Неинициализированное  <br/> |
   
## <a name="see-also"></a>См. также



[Нормальное состояние](normal-state.md)
  
[Состояния форм](form-states.md)

