---
title: Доступные события и их идентификаторы DISPID (экспортированные API Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: В этом разделе описываются идентификаторы диспетчеризации для событий, которые Outlook делает доступным.
ms.openlocfilehash: 31843a2eb8f91eabdc0dbf54a269270eb172baa7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316879"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>Доступные события и их идентификаторы DISPID (экспортированные API Outlook)

В этом разделе описываются идентификаторы диспетчеризации для событий, которые Outlook делает доступным.
  
Outlook предоставляет следующие идентификаторы диспетчеризации (DISPID), позволяющие надстройкам C++ прослушивать и обрабатывать соответствующие события из функции [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) . 
  
|**Константа**|**DISPID для события**|**Описание**|**Параметры**|**Замечания**|
|:-----|:-----|:-----|:-----|:-----|
|**Диспидбефорепринт** <br/> |0xFC8E  <br/> |Используется для обработки события уровня приложения из функции **IDispatch:: Invoke** , которая срабатывает перед выполнением операции печати.  <br/> | Существует два неименованных параметра:  <br/>  Первый параметр имеет тип * * ВТ_БУЛ|ВТ_БРЕФ * *. Чтобы отменить событие, в этом параметре возвращается значение **VARIANT_TRUE** .  <br/>  Второй параметр не используется и должен игнорироваться.  <br/> |Этот идентификатор DISPID доступен с момента создания Outlook 2010.  <br/> |
|**Диспидевентреадкомплете** <br/> |0xFC8F  <br/> |Используется для обработки события уровня элемента из функции **Invoke:: Invoke** , которая срабатывает после того, как приложение Outlook завершило чтение свойств элемента.  <br/> |Существует только один параметр _Cancel_ , имеющий тип * * вт_бул|ВТ_БРЕФ * *. Чтобы отменить операцию чтения, в этом параметре возвращается значение **VARIANT_TRUE** .  <br/> |Этот идентификатор DISPID доступен с момента создания Outlook 2010.  <br/> Это событие относится к событию ЕЦЕ клиентского расширения Exchange () **иексчекстмессажеевентс:: онреадкомплете**, а также к событию **ReadComplete** , которое было добавлено в объектную модель с момента создания Outlook 2013.  <br/> |
   
Пример использования DISPID для прослушивания и обработки события приведен в описании `CAppEventListener::Invoke` функции в решении Outlook для C++, описанном в статье [Реализация приемников событий Outlook 2002/XP в MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C).
  
## <a name="see-also"></a>См. также

- [Экспортированные API Outlook](outlook-exported-apis.md)
- [Constants (Outlook exported APIs)](constants-outlook-exported-apis.md)
- [Сведения об интерфейсах API, экспортируемых Outlook](about-apis-exported-by-outlook.md)
- [Реализация приемников событий Outlook 2002 и XP в MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

