---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Поддерживает переостережку встреч в папке календаря.
ms.openlocfilehash: cf4f7c790a8561f149160c83418a0d5ebd91a455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410072"
---
# <a name="iolkapptrebaser"></a>IOlkApptRebaser

Поддерживает переостережку встреч в папке календаря.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследуется от:  <br/> |**IUnknown** <br/> |
|Файл заголовка:  <br/> |tzmovelib.h  <br/> |
|Реализовано в:  <br/> |tzmovelib.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения MAPI  <br/> |
|В:  <br/> |Объект outlook rebasing  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)** <br/> |Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.  <br/> |
|**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)** <br/> |Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.  <br/> |
|**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)** <br/> |Начинает задачу по переоплате встреч с учетом списка встреч, обычно полученных из **EndEnumerateAppointments.**  <br/> |
|**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)** <br/> |Waits for appointment rebasing to complete and retrieves the results.  <br/> |
   
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

