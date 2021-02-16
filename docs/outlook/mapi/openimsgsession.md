---
title: OpenIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenIMsgSession
api_type:
- COM
ms.assetid: f75229e3-5f44-4298-8706-9eddf0ef124c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326196"
---
# <a name="openimsgsession"></a>OpenIMsgSession

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает и открывает сеанс сообщений, в который будут сгруппы сообщения, созданные в нем. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Imessage.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a>Параметры

 _lpMalloc_
  
> [in] Указатель на объект-память для размещения интерфейса OLE [IMalloc.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) MAPI должен использовать этот метод выделения при работе с интерфейсом OLE [IStorage.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����. 
    
 _lppMsgSess_
  
> [out] Указатель на указатель на возвращенный объект сеанса сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Сеанс открыт.
    
MAPI_E_INVALID_PARAMETER
  
>  _lpMalloc_ или  _lppMsgSess имеет_ NULL. 
    
MAPI_E_INVALID_FLAGS
  
> Были переданы недопустимые флаги.
    
MAPI_UNICODE
  
> При вызове этой функции клиент или поставщик услуг устанавливает флаг MAPI_UNICODE для создания MSG-файлов Юникода. В [итоговом файле Imessage](imessageimapiprop.md) STORE_UNICODE_OK в PR_STORE_SUPPORT_MASK поддерживаются свойства Юникод. 
    
## <a name="remarks"></a>Примечания

Сеанс сообщений используется клиентские приложения и поставщики служб, которые хотят иметь дело с несколькими связанными объектами MAPI [IMessage: IMAPIProp,](imessageimapiprop.md) построенными на основе объектов OLE **IStorage.** Клиент или поставщик использует функции **OpenIMsgSession** и [CloseIMsgSession](closeimsgsession.md) для переноса создания таких сообщений в сеансе сообщений. После открытия сеанса сообщения клиент или поставщик передает ему указатель в [вызове OpenIMsgOnIStg](openimsgonistg.md) для создания нового объекта **IMessage**-on-IStorage.  
  
Сеанс сообщения отслеживает все объекты **IMessage** **-on-IStorage,** созданные во время сеанса, а также все вложения и другие свойства сообщений. Когда клиент или поставщик вызывает **CloseIMsgSession,** он закрывает все эти объекты. Вызов **CloseIMsgSession** — единственный способ закрыть **объекты IMessage**-on-IStorage.  
  
 **OpenIMsgSession** используется клиентами и поставщиками, которые требуют возможности обработки нескольких связанных сообщений в качестве объектов **OLE IStorage.** Если одновременно нужно открыть только одно такое сообщение, нет необходимости отслеживать несколько сообщений и нет причин создавать сеанс сообщений с **помощью OpenIMsgSession.** 
  
Так как он имеет дело с объектом OLE, MAPI должен использовать выделение памяти OLE. Дополнительные сведения об объектах OLE, структурированных хранилищах и выделении памяти OLE, см. в [OLE и передаче данных.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx) 
  

