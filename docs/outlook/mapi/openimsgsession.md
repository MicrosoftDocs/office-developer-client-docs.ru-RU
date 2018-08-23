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
ms.openlocfilehash: 39dd053b2896ebcfcdec97d976af3e75e19f8c0b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564957"
---
# <a name="openimsgsession"></a>OpenIMsgSession

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Создает и открывает сеанс сообщения с группировкой сообщения, создаваемые в ней. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |IMessage.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a>Параметры

 _lpMalloc_
  
> [in] Указатель на объект распределителя памяти, предоставление интерфейса OLE [IMalloc](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-imalloc) . Необходимо использовать этот метод для распределения при работе с помощью интерфейса OLE [IStorage](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-istorage) MAPI. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����. 
    
 _lppMsgSess_
  
> [out] Указатель на указатель на объект сеанса возвращенных сообщений.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Сеанс был открыт.
    
MAPI_E_INVALID_PARAMETER
  
>  _lpMalloc_ или _lppMsgSess_ имеет значение NULL. 
    
MAPI_E_INVALID_FLAGS
  
> Переданы недопустимые флаги.
    
MAPI_UNICODE
  
> При вызове этой функции клиента или поставщика задается флаг MAPI_UNICODE для создания файлов MSG-файл в кодировке Юникод. Созданный файл [Imessage](imessageimapiprop.md) показывает STORE_UNICODE_OK в его PR_STORE_SUPPORT_MASK и поддерживает Юникод свойства. 
    
## <a name="remarks"></a>Замечания

Сеанса сообщения используется клиентскими приложениями, а также поставщиков услуг, чтобы работать с несколькими соответствующие MAPI [IMessage: IMAPIProp](imessageimapiprop.md) объекты, построенные на основе базовых объектов OLE **IStorage** . Клиента или поставщика с помощью функции **OpenIMsgSession** и [CloseIMsgSession](closeimsgsession.md) для создания таких сообщений во время сеанса сообщения. После запуска сеанса сообщения клиента или поставщика передает указатель на него в вызове [OpenIMsgOnIStg](openimsgonistg.md) для создания нового **IMessage**- на - **IStorage** объект. 
  
Сообщение сеанса хранит информацию о всех **IMessage**- on - **IStorage** объекты, созданные во время на протяжении сеанса, помимо все вложения и другие свойства сообщений. Когда клиента или поставщика вызывает **CloseIMsgSession**, закрывает все эти объекты. Вызов **CloseIMsgSession** — это единственный способ закрыть **IMessage**- on - **IStorage** объекты. 
  
 **OpenIMsgSession** используется клиентов и поставщиков, которым требуется возможность обработки нескольких связанных сообщений как объекты OLE **IStorage** . Если только одного сообщения должны быть открыты одновременно, нет необходимости для отслеживания нескольких сообщений и нет причин для создания сеанса сообщения с **OpenIMsgSession**. 
  
Так как иметь дело с базовым объектом OLE, MAPI необходимо использовать выделения памяти для OLE. Дополнительные сведения об объектах СТРУКТУРИРОВАННОГО хранилища и выделение памяти OLE можно [OLE и передачи данных](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  

