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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432949"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет предварительные сведения, написанные функцией [preprocessMessage](preprocessmessage.md) из сообщения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Определенные функции, реализованные в:  <br/> |Поставщики транспорта  <br/> |
|Определенная функция, вызванная:  <br/> |Шпалер MAPI  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> [in] Указатель на предварительное сообщение, из которого должна быть удалена информация.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Предварительная информация была успешно удалена.
    
## <a name="remarks"></a>Примечания

Spooler MAPI вызывает функцию на основе **RemovePreprocessInfo**. Поставщик транспорта регистрирует функцию **RemovePreprocessInfo** одновременно с регистрацией параллельной функции **preprocessMessage** в вызове метода [IMAPISupport::RegisterPreprocessor.](imapisupport-registerpreprocessor.md) 
  
Визуализация изображения, пригодная для передачи факса, является примером предварительной подготовки сведений, написанных функцией, определенной прототипом функции [PreprocessMessage.](preprocessmessage.md) Spooler MAPI обычно вызывает функцию **RemovePreprocessInfo** после отправки сообщения, которое содержит предварительно отображленную информацию. 
  

