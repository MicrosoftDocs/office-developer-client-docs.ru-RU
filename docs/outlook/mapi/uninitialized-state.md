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
ms.openlocfilehash: 95ed80a6d0ea6a6a7c8cc768b32981ac899b69e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578250"
---
# <a name="uninitialized-state"></a>Неинициализированное состояние

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Неинициализированная переменная состояние — исходное состояние формы, в которой должны быть объекты при первом создании. Объекты формы становятся инициализирован с данными сообщения при клиентского приложения вызывается метод [IPersistMessage::InitNew](ipersistmessage-initnew.md) или [IPersistMessage::Load](ipersistmessage-load.md) объекта формы. В следующей таблице описываются допустимые переходы из состояния Unitialized. 
  
|**Метод IPersistMessage**|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Загрузите объект формы с данными по умолчанию.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Загрузите объект формы с данными из целевого сообщения.  <br/> |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Возвращает успешно, или значение последней ошибки и возвратить значение E_UNEXPECTED.  <br/> |Неинициализированная переменная  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращает последнюю ошибку.  <br/> |Неинициализированная переменная  <br/> |
|Другие [IPersistMessage: IUnknown](ipersistmessageiunknown.md) методы или методы от других интерфейсов  <br/> |Значение последней ошибки и возвратить значение E_UNEXPECTED.  <br/> |Неинициализированная переменная  <br/> |
   
## <a name="see-also"></a>См. также



[Обычное состояние](normal-state.md)
  
[Состояния форм](form-states.md)

