---
title: Состояние HandsOffFromNormal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426473"
---
# <a name="handsofffromnormal-state"></a>Состояние HandsOffFromNormal

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Состояние HandsOffFromNormal очень похоже на состояние [HandsOffAfterSave](handsoffaftersave-state.md) . Это часть процесса сохранения содержимого формы в постоянном хранилище. В этом состоянии объект Form должен относиться к изменениям копий значений свойств сообщения в памяти, так как эти изменения могут быть недоступны другим пользователям. В следующей таблице описаны допустимые переходы из состояния HandsOffFromNormal. 
  
|Иперсистмессаже * * метод * *|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[Иперсистмессаже:: савекомплетед](ipersistmessage-savecompleted.md) (_пмессаже! =_ null)  <br/> |Замените сообщение объекта Message на _пмессаже_, заменяющее сообщение, которое было отозвано предыдущим вызовом метода [Иперсистмессаже:: хандсоффмессаже](ipersistmessage-handsoffmessage.md). Данные в новом сообщении гарантированно совпадают с теми, что и в отозванном сообщении. Сообщение не должно быть помечено как Clean, и не должно [имапивиевадвисесинк:: OnSave](imapiviewadvisesink-onsaved.md) вызывается после этого вызова. Если вызов **савекомплетед** выполнен успешно, введите нормальное [](normal-state.md) состояние. В противном случае Оставайтесь в состоянии HandsOffFromNormal.  <br/> |Обычный или HandsOffFromNormal  <br/> |
|**Иперсистмессаже:: савекомплетед** (_пмессаже = =_ null)  <br/> |Задайте для последней ошибки значение Е_УНЕКСПЕКТЕД.  <br/> |HandsOffFromNormal  <br/> |
|**Хандсоффмессаже**, [Иперсистмессаже:: Save](ipersistmessage-save.md), [Иперсистмессаже:: Инитнев](ipersistmessage-initnew.md)или [иперсистмессаже:: Load](ipersistmessage-load.md) <br/> |Задайте для последней ошибки значение Е_УНЕКСПЕКТЕД.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возврат последней ошибки.  <br/> |HandsOffFromNormal  <br/> |
|Другие [иперсистмессаже:](ipersistmessageiunknown.md) методы или методы IUnknown из других интерфейсов  <br/> |Задайте для последней ошибки значение Е_УНЕКСПЕКТЕД.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>См. также



[Состояния форм](form-states.md)

