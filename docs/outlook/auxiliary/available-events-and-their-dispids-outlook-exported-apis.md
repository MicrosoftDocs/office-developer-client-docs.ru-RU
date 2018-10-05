---
title: Доступные события и их идентификаторы DISPID (Outlook экспортировать API-интерфейсы)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: В этом разделе описываются идентификаторы диспетчера для событий, которые Outlook делает доступными.
ms.openlocfilehash: 31843a2eb8f91eabdc0dbf54a269270eb172baa7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400238"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>Доступные события и их идентификаторы DISPID (Outlook экспортировать API-интерфейсы)

В этом разделе описываются идентификаторы диспетчера для событий, которые Outlook делает доступными.
  
Outlook предоставляет следующие идентификаторов отправки (DISPID) чтобы разрешить надстройки C++ для прослушивания и обработки соответствующих событий из функции [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) . 
  
|**Constant**|**DISPID для события**|**Описание**|**Параметры**|**Замечания**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Используется для обработки событий уровня приложения из функции **IDispatch::Invoke** , которое вызывается перед операцией печати.  <br/> | Существует 2 неименованные параметры.  <br/>  Первый параметр имеет тип ** VT_BOOL|VT_BREF **. Возврат **VARIANT_TRUE** в этот параметр, чтобы отменить событие.  <br/>  Второй параметр не используется и его следует игнорировать.  <br/> |В этом dispid доступна начиная с Outlook 2010.  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Используется для обработки событий на уровне элементов из функции **IDispatch::Invoke** , которое вызывается после завершения чтение свойств элемента Outlook.  <br/> |Имеется только один параметр, _Отменить_ которой имеет тип ** VT_BOOL|VT_BREF **. Возврат **VARIANT_TRUE** в этот параметр, чтобы отменить операцию чтения.  <br/> |В этом dispid доступна начиная с Outlook 2010.  <br/> Это событие соответствует **IExchExtMessageEvents::OnReadComplete**события расширения клиента Exchange (ECE), а также к **ReadComplete** события, который был добавлен в объектную модель с момента Outlook 2013.  <br/> |
   
Примеры использования dispid прослушивать и обрабатывать события, представлены в разделе `CAppEventListener::Invoke` функции в решении C++ Outlook, описанных в [Реализации Outlook 2002/XP приемников событий, в MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C).
  
## <a name="see-also"></a>См. также

- [Экспортированные API Outlook](outlook-exported-apis.md)
- [Constants (Outlook exported APIs)](constants-outlook-exported-apis.md)
- [Сведения об интерфейсах API, экспортируемых Outlook](about-apis-exported-by-outlook.md)
- [Реализация событий Outlook 2002/XP приемников в MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

