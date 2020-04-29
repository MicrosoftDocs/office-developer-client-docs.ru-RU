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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет функцию обратного вызова, которая может освобождать интерфейс **IStorage** после окончательного выпуска объекта **iMessage** , построенного на основе функции [опенимсгонистг](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |IMessage. h  <br/> |
|Определенная функция реализована следующим образом:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
|Определенная функция, вызываемая:  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>Параметры

 _улкаллердата_
  
> возврата Содержит сведения о вызывающем приложении для интерфейса **iMessage** . 
    
 _лпмессаже_
  
> возврата Указатель на сообщение верхнего уровня и вложения, которые были выпущены.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  

