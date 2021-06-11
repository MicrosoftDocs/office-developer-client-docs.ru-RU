---
title: MSGCALLRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9ffaab1e9cc381be2abfb389f4b72067dca2438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405914"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет функцию вызова, которая может освободить **интерфейс IStorage** после окончательного выпуска объекта **IMessage,** построенного поверх него с помощью функции [OpenIMsgOnIStg.](openimsgonistg.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Imessage.h  <br/> |
|Определенные функции, реализованные в:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
|Определенная функция, вызванная:  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>Parameters

 _ulCallerData_
  
> [in] Содержит сведения о вызываемом приложении **об интерфейсе IMessage.** 
    
 _lpMessage_
  
> [in] Указатель на выпущенное сообщение верхнего уровня и вложения.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  

