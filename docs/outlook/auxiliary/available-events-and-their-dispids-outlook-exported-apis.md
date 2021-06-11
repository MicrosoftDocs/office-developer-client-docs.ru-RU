---
title: Доступные события и их удлиняется (Outlook экспортируются API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: В этом разделе описываются идентификаторы отправки для событий, которые Outlook доступны.
ms.openlocfilehash: 31843a2eb8f91eabdc0dbf54a269270eb172baa7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316879"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>Доступные события и их удлиняется (Outlook экспортируются API)

В этом разделе описываются идентификаторы отправки для событий, которые Outlook доступны.
  
Outlook предоставляет следующие идентификаторы отправки (отчаялись), чтобы разрешить надстройке C++ прослушивать и обрабатывать соответствующие события из функции [IDispatch::Invoke.](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) 
  
|**Константа**|**Dispid for event**|**Описание**|**Параметры**|**Замечания**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Используется для обработки события на уровне приложений из функции **IDispatch::Invoke,** которая загорелась перед операцией печати.  <br/> | Существует 2 неназванных параметра:  <br/>  Первый параметр — тип **VT_BOOL|VT_BREF**. Возврат **VARIANT_TRUE** в этом параметре, чтобы отменить событие.  <br/>  Второй параметр не используется и должен игнорироваться.  <br/> |Это отвяхлое доступно с 2010 Outlook 2010 г.  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Используется для обработки события на уровне элемента из функции **IDispatch::Invoke,** которая Outlook после завершения чтения свойств элемента.  <br/> |Существует только один параметр  _Cancel,_ который имеет тип **VT_BOOL|VT_BREF**. Возврат **VARIANT_TRUE** в этом параметре, чтобы отменить операцию чтения.  <br/> |Это отвяхлое доступно с 2010 Outlook 2010 г.  <br/> Это событие соответствует событию Exchange клиентских расширений (ECE) **IExchExtMessageEvents::OnReadComplete,** а также событию **ReadComplete,** которое было добавлено в объектную модель с Outlook 2013 г.  <br/> |
   
Пример использования неумелого для прослушивания и обработки события см. в описании функции решения C++ Outlook, описанного в решении `CAppEventListener::Invoke` [Implementing Outlook 2002/XP Event Sinks in MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C).
  
## <a name="see-also"></a>См. также

- [Экспортированные API Outlook](outlook-exported-apis.md)
- [Constants (Outlook exported APIs)](constants-outlook-exported-apis.md)
- [Сведения об интерфейсах API, экспортируемых Outlook](about-apis-exported-by-outlook.md)
- [Реализация Outlook событий 2002/XP в MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

