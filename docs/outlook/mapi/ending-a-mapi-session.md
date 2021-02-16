---
title: Завершение сеанса MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 74c2a7247df02570761247a9e4a6fae378f37312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287155"
---
# <a name="ending-a-mapi-session"></a>Завершение сеанса MAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиенты могут закончить свои сеансы в ответ на запрос пользователя сразу же или после обработки всех исходящие сообщения, а также при критических ошибках. Некоторые клиенты должны оставаться в системе, чтобы ожидающие исходящие сообщения могли связаться с поставщиком транспорта и системой обмена сообщениями назначения. Если такой клиент отправляет сообщение и сразу же выходит из нее, то сообщение может оставаться в исходякой очереди до тех пор, пока пользователь не снова войдите в систему и не войдите в систему достаточно долго, чтобы сообщение было передано.
  
 **Когда необходимо завершить сеанс подсистемой MAPI**
  
1. Отмените регистрации для всех уведомлений, вызывая метод **Unadvise** каждого зарегистрированного объекта. 
    
2. Освободите все открытые объекты, вызывая их методы [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) Типы открытых объектов могут включать приемники консультаций, таблицу состояния, папку "Outbox", одно или несколько хранилищ сообщений и адресную книгу. 
    
3. Вызовите [MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить память для всех кэшных идентификаторов записей, таких как **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId).](pidtagipmsubtreeentryid-canonical-property.md)
    
4. Call [IMAPISession::Logoff](imapisession-logoff.md), setting the MAPI_LOGOFF_UI flag if you allow a user interface and the MAPI_LOGOFF_SHARED flag if you own the current shared session. **При этом** всем другим клиентам, использующим текущий общий сеанс, сообщается, что они должны выйти из системы, отправив уведомление об ошибке. 
    
5. Освободите указатель сеанса, вызывая метод **IUnknown::Release** сеанса. 
    
6. Если вы вызывали [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) во время запуска сеанса для инициализации библиотек OLE, теперь не инициализируют их, вызывая [OleUninitialize.](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx) Только клиенты, которые **вызывали OleInitialize,** должны **вызывать OleUninitialize.** 
    
7. Uninitialize the MAPI libraries by calling [MAPIUninitialize](mapiuninitialize.md). Если в какой-то момент вы вызывали **OleInitialize,** убедитесь, что перед вызовом **MAPIUninitialize** происходит вызов **OleUninitialize.** Временные рамки очень важны. Если вызов **OleUninitialize** следует за вызовом **MAPIUninitialize,** клиент может завершиться не по-разому. 
    
8. Если вы [вызывали ScInitMapiUtil](scinitmapiutil.md) во время запуска сеанса, чтобы инициализировать библиотеку utility MAPI, теперь не инициализировать ее, вызывая [DeinitMapiUtil](deinitmapiutil.md). Только клиенты, которые вызвали **ScInitMapiUtil,** должны вызывать **DeinitMapiUtil.**
    
> [!NOTE]
> Все открытые объекты должны быть отпущены перед вызовом **IMAPISession::Logoff.** Объекты, которые остаются открытыми после **того,** как выйдите из нее, становятся недопустимыми; они не могут принимать вызовы и могут никогда не быть освобождены. При вызове одного из этих объектов ожидается сбой вызова. 
  
 MAPI не имеет механизма удаления DLL в процессе завершения сеанса. DLL поставщика услуг можно удалить только в том случае, если клиент конфигурации, например панель управления, вызывает функцию точки входа службы сообщений с MSG_SERVICE_INSTALL события. 
  

