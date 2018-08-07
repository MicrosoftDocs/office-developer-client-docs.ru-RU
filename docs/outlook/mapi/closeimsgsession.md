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
ms.openlocfilehash: c190691c8cfcb9b049bcf9ee4f21436e20955def
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808167"
---
# <a name="closeimsgsession"></a>CloseIMsgSession

  
  
**Относится к**: Outlook 
  
Закрывает сеанса сообщения и все сообщения, созданные в течение этого сеанса. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |IMessage.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a>Параметры

 _lpMsgSess_
  
> [in] Указатель на объект сеанса сообщения, полученные с помощью функции [OpenIMsgSession](openimsgsession.md) в начале сеанса сообщения. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Сообщение сеанса используется клиентскими приложениями и поставщиками услуг, которые хотите работать с нескольких связанных объектов MAPI **IMessage** , построенные базовые объекты OLE **IStorage** . Клиента или поставщика с помощью функции [OpenIMsgSession](openimsgsession.md) и **CloseIMsgSession** для создания таких сообщений во время сеанса сообщения. После запуска сеанса сообщения клиента или поставщика передает указатель на него в вызове [OpenIMsgOnIStg](openimsgonistg.md) для создания нового **IMessage**- на - **IStorage** объект. 
  
Сообщение сеанса хранит информацию о всех объектов **IMessage**- on - **IStorage** , открытых в течение сеанса, помимо все вложения и другие свойства сообщений. Когда клиента или поставщика вызывает **CloseIMsgSession**, закрывает все эти объекты. Вызов **CloseIMsgSession** — это единственный способ закрыть **IMessage**- on - **IStorage** объекты. 
  

