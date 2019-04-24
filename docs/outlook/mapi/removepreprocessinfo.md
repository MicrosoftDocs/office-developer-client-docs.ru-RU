---
title: RemovePreprocessInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.RemovePreprocessInfo
api_type:
- COM
ms.assetid: 25f46937-abac-4a0b-83db-eeac9451c112
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d80c73aef780a0da39f3939f71462488a067de5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328380"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет предварительно обработанные сведения, записанные функцией на основе [препроцессмессаже](preprocessmessage.md) , из сообщения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Маписпи. h  <br/> |
|Определенная функция реализована следующим образом:  <br/> |Поставщики транспорта  <br/> |
|Определенная функция, вызываемая:  <br/> |Диспетчер очереди MAPI  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Параметры

 _Лпмессаже_
  
> возврата Указатель на предварительно обработанное сообщение, из которого удаляются сведения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Предварительная обработка данных успешно удалена.
    
## <a name="remarks"></a>Комментарии

Диспетчер очереди MAPI вызывает функцию на основе **ремовепрепроцессинфо**. Поставщик транспорта регистрирует функцию **ремовепрепроцессинфо** в то же время, когда она регистрирует параллельную функцию **препроцессмессаже** в вызове метода [имаписуппорт:: регистерпрепроцессор](imapisupport-registerpreprocessor.md) . 
  
Визуализация изображений, подходящая для передачи факсов, это пример предварительно обработанной информации, записанной функцией, определенной прототипом функции [препроцессмессаже](preprocessmessage.md). Диспетчер очереди MAPI обычно вызывает функцию **ремовепрепроцессинфо** после отправки сообщения, которое содержит предварительно обработанные сведения. 
  

