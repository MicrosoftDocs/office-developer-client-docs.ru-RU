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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: aaa1adaa170349c3df3a2256802a502cb2512b20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810024"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**Применимо к**: Outlook 
  
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

## <a name="parameters"></a>Parameters

 _ulCallerData_
  
> [in] Содержит вызывающего приложения сведения об интерфейсе **IMessage** . 
    
 _lpMessage_
  
> [in] Указатель на верхнего уровня сообщений и вложений, которые были выпущены.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  

