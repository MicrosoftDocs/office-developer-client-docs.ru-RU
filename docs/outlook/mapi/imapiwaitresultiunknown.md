---
title: 'IMAPIWaitResult : IUnknown'
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: d7157f57-709d-4e53-973b-176954e2bb73
description: IMAPIWaitResult
Last modified: April 26, 2021
ms.openlocfilehash: 67a0fffdd0ab6d4989c12568f4d89808ba5adc7a
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062041"
---
# <a name="imapiwaitresult--iunknown"></a>IMAPIWaitResult : IUnknown
  
**Применяется к**: Outlook 2013 | Outlook 2016 | Outlook 2019 г.

Этот интерфейс используется пользователями IMAPIInitMonitor для управления, где происходит ожидание. Это позволяет им создавать объект на одном потоке и перемещать его другим потоком для выполнения фактического ожидания.

## <a name="vtable-order"></a>Заказ Vtable

| функция | description |
|:-----|:-----|
|[HRESULT IMAPIWaitResult::End()](imapiwaitresult-end.md)|Вызвано, чтобы инициировать блокировку ожидания в потоке, где он называется, который не должен быть тем же потоком, который называется *IMAPIInitMonitor::BeginWait*.|

| быстрая информация | result |
|:-----|:-----|
|Наследует от:  <br/> |IUnknown  <br/> |
|Реализовано в:  <br/> |  OLMAPI32.DLL<br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIWaitResult  <br/> |

## <a name="see-also"></a>См. также

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[IMAPIInitMonitor : IUnknown](imapiinitmonitoriunknown.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
