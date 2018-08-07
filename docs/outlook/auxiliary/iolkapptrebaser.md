---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Поддерживает повторного размещения en встреч в папке календаря.
ms.openlocfilehash: 57ca59121f74c7b64a84282c7493e4aed3179f7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807869"
---
# <a name="iolkapptrebaser"></a>IOlkApptRebaser

Поддерживает повторного размещения en встреч в папке календаря.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |**Интерфейс IUnknown** <br/> |
|Файл заголовка:  <br/> |tzmovelib.h  <br/> |
|Реализованный:  <br/> |tzmovelib.dll  <br/> |
|Вызывается:  <br/> |Клиентские приложения MAPI  <br/> |
|Предоставляется для:  <br/> |Объект сдвига Outlook  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)** <br/> |Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.  <br/> |
|**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)** <br/> |Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.  <br/> |
|**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)** <br/> |Начинается задач для повторного размещения встречи en список встреч, обычно получили от **EndEnumerateAppointments**.  <br/> |
|**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)** <br/> |Waits for appointment rebasing to complete and retrieves the results.  <br/> |
   
## <a name="see-also"></a>См. также

- [About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

