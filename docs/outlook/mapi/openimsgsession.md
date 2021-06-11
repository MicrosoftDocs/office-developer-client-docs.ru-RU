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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает и открывает сеанс сообщений, который группит созданные в нем сообщения. 
  
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

## <a name="parameters"></a>Parameters

 _lpMalloc_
  
> [in] Указатель на объект-аллигатор памяти, подвергая обнажает интерфейс OLE [IMalloc.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) MAPI должен использовать этот метод выделения при работе с интерфейсом [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) OLE. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����. 
    
 _lppMsgSess_
  
> [вышел] Указатель на указатель на объект сеанса возвращенного сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Сеанс был открыт.
    
MAPI_E_INVALID_PARAMETER
  
>  _lpMalloc_ или  _lppMsgSess_ — это NULL. 
    
MAPI_E_INVALID_FLAGS
  
> Были переданы недействительные флаги.
    
MAPI_UNICODE
  
> При вызове этой функции клиент или поставщик услуг задает флаг MAPI_UNICODE для создания файлов Unicode .msg. В результате файл [Imessage](imessageimapiprop.md) STORE_UNICODE_OK в PR_STORE_SUPPORT_MASK поддерживает свойства Unicode. 
    
## <a name="remarks"></a>Примечания

Сеанс сообщений используется клиентских приложений и поставщиков услуг, которые хотят иметь дело с несколькими связанными объектами [MAPI IMessage: IMAPIProp,](imessageimapiprop.md) построенными на основе встроенных объектов **IStorage** OLE. Клиент или поставщик используют функции **OpenIMsgSession** и [CloseIMsgSession](closeimsgsession.md) для упаковки создания таких сообщений в сеансе сообщений. После открытия сеанса сообщений клиент или поставщик передает ему указатель в [вызове в OpenIMsgOnIStg](openimsgonistg.md) для создания нового **объекта IMessage**-on-IStorage.  
  
Сеанс сообщений отслеживает все **объекты IMessage**-on-IStorage, созданные во время сеанса, а также все вложения и другие свойства сообщений.  Когда клиент или поставщик вызывает **CloseIMsgSession,** он закрывает все эти объекты. Вызов **CloseIMsgSession** — это единственный способ закрыть **объекты IMessage-on-IStorage.**  
  
 **OpenIMsgSession** используется клиентами и поставщиками, которые требуют возможности обрабатывать несколько связанных сообщений в качестве объектов **IStorage** OLE. Если одновременно должно быть открыто только одно такое сообщение, нет необходимости отслеживать несколько сообщений и нет причин создавать сеанс сообщений с **openIMsgSession.** 
  
Так как он имеет дело с объектом OLE, MAPI должна использовать распределение памяти OLE. Дополнительные сведения о структурированных объектах хранения OLE и распределении памяти OLE см. в [OLE и Data Transfer.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx) 
  

