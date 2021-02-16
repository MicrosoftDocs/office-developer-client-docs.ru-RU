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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Удаляет предварительно запроцесснутую информацию, написанную функцией на основе [PreprocessMessage,](preprocessmessage.md) из сообщения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Определяемая функция, реализованная в:  <br/> |Поставщики транспорта  <br/> |
|Определяемая функция, вызванная:  <br/> |MapI spooler  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Параметры

 _lpMessage_
  
> [in] Указатель на предварительное сообщение, из которого следует удалить информацию.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Предварительно обучаемая информация была успешно удалена.
    
## <a name="remarks"></a>Примечания

Пулер MAPI вызывает функцию на основе **RemovePreprocessInfo.** Поставщик транспорта регистрирует функцию на основе **RemovePreprocessInfo** одновременно с регистрацией параллельной функции на основе **PreprocessMessage** в вызове метода [IMAPISupport::RegisterPreprocessor.](imapisupport-registerpreprocessor.md) 
  
Отрисовка изображения, подходящая для передачи факсов, является примером предварительной подготовки информации, написанной функцией, определенной прототипом функции [PreprocessMessage.](preprocessmessage.md) Пулер MAPI обычно вызывает функцию **RemovePreprocessInfo** после отправки сообщения с предварительной подготовкой информации. 
  

