---
title: Состояние HandsOffAfterSave
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299526"
---
# <a name="handsoffaftersave-state"></a>Состояние HandsOffAfterSave

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Состояние HandsOffAfterSave является частью процесса сохранения содержимого формы в постоянном хранилище. В этом состоянии объект Form должен относиться к изменениям копий значений свойств сообщения в памяти, так как эти изменения могут быть недоступны другим пользователям. В следующей таблице описаны допустимые переходы из состояния HandsOffAfterSave.
  
|**Метод Иперсистмессаже**|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[Иперсистмессаже:: савекомплетед](ipersistmessage-savecompleted.md) (_пмессаже! =_ null)  <br/> |Откройте все внедренные объекты. Данные в сообщениях, хранящихся в _пмессаже_ , гарантированно совпадают с сообщением в предыдущем вызове [Иперсистмессаже:: Save](ipersistmessage-save.md) . Если вызов **савекомплетед** выполнен успешно, введите нормальное состояние. В противном случае установите для последней ошибки значение E_OUTOFMEMORY и оставайтесь в состоянии HandsOffAfterSave.  <br/> |[Обычный](normal-state.md) или HandsOffAfterSave  <br/> |
|**Иперсистмессаже:: савекомплетед** (_пмессаже = =_ null)  <br/> |Задайте для последней ошибки значение Е_ИНВАЛИДАРГ или Е_УНЕКСПЕКТЕД.  <br/> |HandsOffAfterSave  <br/> |
|[Иперсистмессаже:: хандсоффмессаже](ipersistmessage-handsoffmessage.md), **Save**или [иперсистмессаже:: инитнев](ipersistmessage-initnew.md) <br/> |ПриСвойте последней ошибке значение и возвратите Е_УНЕКСПЕКТЕД.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Загрузка объекта Form с данными из целевого сообщения. Этот вызов может произойти, когда объект Form переходит к следующему или предыдущему сообщению в папке.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возврат последней ошибки.  <br/> |HandsOffAfterSave  <br/> |
|Другие [иперсистмессаже:](ipersistmessageiunknown.md) методы или методы IUnknown из других интерфейсов  <br/> |ПриСвойте последней ошибке значение и возвратите Е_УНЕКСПЕКТЕД.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>См. также



[Состояния форм](form-states.md)

