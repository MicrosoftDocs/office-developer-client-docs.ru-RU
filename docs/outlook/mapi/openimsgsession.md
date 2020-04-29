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
  
Создает и открывает сеанс сообщений, в котором группируются сообщения, созданные в нем. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |IMessage. h  <br/> |
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

 _лпмаллок_
  
> возврата Указатель на объект распределителя памяти, который предоставляет интерфейс для [выделения](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) OLE. При работе с интерфейсом OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) для MAPI необходимо использовать этот метод распределения. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����. 
    
 _лппмсгсесс_
  
> вышли Указатель на указатель на возвращенный объект сеанса сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Сеанс открыт.
    
MAPI_E_INVALID_PARAMETER
  
>  _лпмаллок_ или _лппмсгсесс_ имеет значение null. 
    
MAPI_E_INVALID_FLAGS
  
> Переданы недопустимые флаги.
    
MAPI_UNICODE
  
> При вызове этой функции клиент или поставщик услуг устанавливает флаг MAPI_UNICODE, чтобы создать файлы Unicode. MSG. Полученный в результате файл [iMessage](imessageimapiprop.md) показывает STORE_UNICODE_OK в PR_STORE_SUPPORT_MASK и поддерживает свойства Юникода. 
    
## <a name="remarks"></a>Примечания

Сеанс сообщений используется клиентскими приложениями и поставщиками услуг, которые хотят работать с несколькими связанными объектами MAPI [iMessage: IMAPIProp](imessageimapiprop.md) , построенными на основе базовых объектов OLE **IStorage** . Клиент или поставщик использует функции **опенимсгсессион** и [клосеимсгсессион](closeimsgsession.md) , чтобы создать оболочку для создания таких сообщений в сеансе сообщений. После открытия сеанса сообщения клиент или поставщик передает указатель на него в вызове [опенимсгонистг](openimsgonistg.md) для создания нового объекта **iMessage**-On- **IStorage** . 
  
В сеансе сообщений отслеживается все объекты **iMessage**(ON — **IStorage** ), созданные в течение сеанса, а также все вложения и другие свойства сообщений. Когда клиент или поставщик вызывает **клосеимсгсессион**, он закрывает все эти объекты. Вызов **клосеимсгсессион** является единственным способом закрытия объектов **iMessage**-On- **IStorage** . 
  
 **Опенимсгсессион** используется клиентами и поставщиками, которым требуется возможность обрабатывать несколько связанных сообщений в виде объектов OLE **IStorage** . Если необходимо одновременно открыть только одно такое сообщение, нет необходимости отслеживать несколько сообщений и нет причин создавать сеанс сообщений с **опенимсгсессион**. 
  
Так как он работает с базовым объектом OLE, MAPI должен использовать выделение памяти OLE. Более подробную информацию об объектах структурированного хранилища OLE и выделении памяти OLE можно узнать в статье [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  

