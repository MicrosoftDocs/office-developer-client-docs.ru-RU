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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Закрывает сеанс сообщений и все сообщения, созданные в этом сеансе. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Imessage.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a>Parameters

 _lpMsgSess_
  
> [in] Указатель на объект сеанса сообщений, полученный с помощью [функции OpenIMsgSession](openimsgsession.md) в начале сеанса сообщения. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Сеанс сообщений используется клиентских приложений и поставщиков услуг, которые хотят иметь дело с несколькими связанными объектами **MAPI IMessage,** построенными поверх ole **IStorage.** Клиент или поставщик используют функции [OpenIMsgSession](openimsgsession.md) и **CloseIMsgSession** для упаковки создания таких сообщений в сеансе сообщений. После открытия сеанса сообщений клиент или поставщик передает ему указатель в [вызове в OpenIMsgOnIStg](openimsgonistg.md) для создания нового **объекта IMessage**-on-IStorage.  
  
Сеанс сообщений отслеживает все **объекты IMessage**-on-IStorage, открытые во время сеанса, а также все вложения и другие свойства сообщений.  Когда клиент или поставщик вызывает **CloseIMsgSession,** он закрывает все эти объекты. Вызов **CloseIMsgSession** — это единственный способ закрыть **объекты IMessage-on-IStorage.**  
  

