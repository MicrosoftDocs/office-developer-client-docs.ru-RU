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
ms.openlocfilehash: e9a1c416cbf992c9cbcfb5de42d302ff16e7f521
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573189"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Определяет функцию обратного вызова, можно освободить интерфейс **IStorage** после окончательной версии объекта **IMessage** , построенных на основе его с помощью функции [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |IMessage.h  <br/> |
|Функция реализован:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
|Вызывается функция:  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>Параметры

 _ulCallerData_
  
> [in] Содержит вызывающего приложения сведения об интерфейсе **IMessage** . 
    
 _lpMessage_
  
> [in] Указатель на верхнего уровня сообщений и вложений, которые были выпущены.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  

