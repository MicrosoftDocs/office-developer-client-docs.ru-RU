---
title: 'IMAPIInitMonitor : IUnknown'
manager: lindalu
26ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIInitMonitor
api_type:
- COM
ms.assetid: ad71ea65-394d-4be2-a9da-cd23099bc2cc
description: IMAPIInitMonitor
Last modified: April 26, 2021
ms.openlocfilehash: dd17d50b04755d9d9c2a10a9b02cd821faf1f7ec
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062048"
---
# <a name="imapiinitmonitor--iunknown"></a>IMAPIInitMonitor : IUnknown

**Применяется к**: Outlook 2013 | Outlook 2016 | Outlook 2019 г.

Иногда приложение, которое потребляет MAPI, может потребовать знать, когда инициализация будет завершена. Например, он имеет несколько потоков, которые могут инициализировать MAPI, или в ответ на инициализацию MAPI приложение хотело бы выполнить некоторую работу, но не хочет всегда вращать стек MAPI. Монитор инициализации предоставляет эту функцию с помощью [объекта CreateMAPIInitializationMonitor.](createmapiinitializationmonitor.md)

| быстрая информация | result |
|:-----|:-----|
|Наследует от:  <br/> |IUnknown  <br/> |
|Реализовано в:  <br/> | OLMAPI32.DLL <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIInitMonitor  <br/> |

## <a name="vtable-order"></a>Заказ Vtable

| функция | description |
|:-----|:-----|
|[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md) <br/> |Возвращает текущее состояние инициализации MAPI.  <br/> |
|[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md) <br/> |Инициирует вызов BLOCKING в этом потоке, который возвращается либо после инициализации указанного числа миллисекунд, либо при инициализации MAPI.  INFINITE можно использовать для бесконечного ожидания.  <br/> |
|[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md) <br/> |Начните ожидание инициализации MAPI или указанного числа миллисекунд, которые должны сойти. Это возвращает интерфейс IMAPIWaitResult, который должен иметь "End" для того, чтобы начать ожидание.  Это позволяет звонячему управлять тем, какой поток заблокирован во время ожидания. <br/> |
