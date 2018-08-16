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
ms.openlocfilehash: fab8860621cee5a87b087ee9d98f373baa278e45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812149"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**Относится к**: Outlook 
  
Удаляет предварительно данные, записанные функцией [PreprocessMessage](preprocessmessage.md) на основе из сообщения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Функция реализован:  <br/> |Поставщиками транспорта  <br/> |
|Вызывается функция:  <br/> |Диспетчер очереди MAPI  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Параметры

 _lpMessage_
  
> [in] Указатель на предварительной обработки сообщений, из которой должна быть удалены сведения.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Сведения о предварительной обработки был удален.
    
## <a name="remarks"></a>Замечания

Диспетчер очереди MAPI вызывает функцию на основании **RemovePreprocessInfo**. Функция **RemovePreprocessInfo** на основе регистрирует поставщика транспорта в то же время, он регистрирует параллельный **PreprocessMessage** на основе функции при вызове метода [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) . 
  
Изображение отображения подходит для передачи факса приведен пример записи функцией, определенные в прототип функции [PreprocessMessage](preprocessmessage.md)предварительной обработки данных. Диспетчер очереди MAPI обычно вызывает функцию **RemovePreprocessInfo** после отправки сообщения, содержащее сведения о предварительной обработки. 
  
