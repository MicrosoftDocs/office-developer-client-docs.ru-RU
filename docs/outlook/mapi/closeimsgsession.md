---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 877bebf0a156c99907505d815ca8d36a4b398678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412039"
---
# <a name="closeimsgsession"></a>CloseIMsgSession

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Закрывает сеанс сообщения и все сообщения, созданные в этом сеансе. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |IMessage. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a>Параметры

 _лпмсгсесс_
  
> возврата Указатель на объект сеанса сообщения, полученный с помощью функции [опенимсгсессион](openimsgsession.md) в начале сеанса сообщения. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Сеанс сообщений используется клиентскими приложениями и поставщиками услуг, которые хотят работать с несколькими связанными объектами MAPI **iMessage** , построенными на основе базовых объектов OLE **IStorage** . Клиент или поставщик использует функции [опенимсгсессион](openimsgsession.md) и **клосеимсгсессион** , чтобы создать оболочку для создания таких сообщений в сеансе сообщений. После открытия сеанса сообщения клиент или поставщик передает указатель на него в вызове [опенимсгонистг](openimsgonistg.md) для создания нового объекта **iMessage**-On- **IStorage** . 
  
В сеансе сообщений отслеживается все объекты **iMessage**(ON — **IStorage** ), открытые в течение сеанса, а также все вложения и другие свойства сообщений. Когда клиент или поставщик вызывает **клосеимсгсессион**, он закрывает все эти объекты. Вызов **клосеимсгсессион** является единственным способом закрытия объектов **iMessage**-On- **IStorage** . 
  

