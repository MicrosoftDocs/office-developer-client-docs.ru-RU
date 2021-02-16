---
title: Доступные события и их dispids (экспортные API Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: В этом разделе описываются идентификаторы диспетчера для событий, которые outlook делает доступными.
ms.openlocfilehash: 31843a2eb8f91eabdc0dbf54a269270eb172baa7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316879"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>Доступные события и их dispids (экспортные API Outlook)

В этом разделе описываются идентификаторы диспетчера для событий, которые outlook делает доступными.
  
Outlook предоставляет следующие идентификаторы диспетчера (dispids), чтобы надстройки C++ прослушивали и обрабатывали соответствующие события из функции [IDispatch::Invoke.](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) 
  
|**Константа**|**Dispid for event**|**Описание**|**Параметры**|**Замечания**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Используется для обработки события уровня приложения из функции **IDispatch::Invoke,** которая сгорает перед операцией печати.  <br/> | Существует 2 неименуемы параметра:  <br/>  Первый параметр имеет тип **VT_BOOL|VT_BREF**. Возвращает **VARIANT_TRUE** в этом параметре, чтобы отменить событие.  <br/>  Второй параметр не используется и должен игнорироваться.  <br/> |This dispid is available since Outlook 2010.  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Используется для обработки события на уровне элемента из функции **IDispatch::Invoke,** которая активна, когда Outlook завершил чтение свойств элемента.  <br/> |Существует только один параметр  _Cancel,_ тип **VT_BOOL|VT_BREF**. Возврат **VARIANT_TRUE** в этом параметре для отмены операции чтения.  <br/> |This dispid is available since Outlook 2010.  <br/> Это событие соответствует событию **IExchExtMessageEvents::OnReadComplete,** а также событию **ReadComplete,** которое было добавлено в объектную модель с outlook 2013.  <br/> |
   
Пример использования отладки для прослушивания и обработки события см. в описании функции в решении C++ Outlook, описанной в реализации событий `CAppEventListener::Invoke` [Outlook 2002/XP в MFC C++ 2003 .NET.](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)
  
## <a name="see-also"></a>См. также

- [Экспортированные API Outlook](outlook-exported-apis.md)
- [Constants (Outlook exported APIs)](constants-outlook-exported-apis.md)
- [Сведения об интерфейсах API, экспортируемых Outlook](about-apis-exported-by-outlook.md)
- [Реализация событий Outlook 2002/XP в MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

