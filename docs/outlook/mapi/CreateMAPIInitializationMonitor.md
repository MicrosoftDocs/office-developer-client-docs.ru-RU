---
title: CreateMAPIInitializationMonitor
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
ms.assetid: 32a9758a-395d-4526-9610-3e4eeaf78c96
description: Монитор инициализации MAPI
Last modified: April 26, 2021
ms.openlocfilehash: da7c48a6b026ccd4cbe4cbac192a1a0760202835
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062055"
---
# <a name="createmapiinitializationmonitor"></a>CreateMAPIInitializationMonitor

**Применяется к**: Outlook 2016 | Outlook 2019 г.
  
## <a name="mapi-initialization-monitor"></a>Монитор инициализации MAPI

Иногда приложение, которое потребляет MAPI, может потребовать знать, когда инициализация будет завершена. Например, он имеет несколько потоков, которые могли бы инициализировать MAPI, или в ответ на инициализацию MAPI приложение хотело бы выполнить некоторую работу, но не хочет всегда вращать стек MAPI. Монитор инициализации предоставляет эту функцию с помощью функции (экспортируемой из OLMAPI32.DLL) и нескольких простых интерфейсов, описанных ниже.

Это точка входа, экспортируемая из OLMAPI32.DLL это позволяет звонячему получить интерфейс для запроса текущего состояния инициализации, установки вызова для завершения инициализации или блокировки текущего потока до завершения. Объект, возвращаемый из этого API, является многоразовым и безопасным для потока и может вызываться из любого потока, а не только из потока, который его извлек. Кроме того, в отличие от других объектов, открытых в MAPI, этот объект действителен до тех пор, пока DLL загружен, его можно повторно использовать в сеансах инициализации и можно потреблять до или после того, как была вызвана MAPIInitialize. Возвращает успех или сбой с помощью стандартного HRESULT com и назначает параметр out экземпляру IMAPIInitMonitor.

```cpp
HRESULT CreateMAPIInitializationMonitor(IMAPIInitMonitor** ppInitMonitor); 
```
#### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor (IMAPIInitMonitor ppInitMonitor)

Эта точка входа, экспортируемая из OLMAPI32.DLL, позволяет вызываемой записи получить интерфейс для запроса текущего состояния инициализации, установки вызова для завершения инициализации или блокировки текущего потока до завершения. Объект, возвращаемый из этого API, является многоразовым и безопасным для потока и может вызываться из любого потока, а не только из потока, который его извлек. Кроме того, в отличие от других объектов, открытых в MAPI, этот объект действителен до тех пор, пока DLL загружен, его можно повторно использовать в сеансах инициализации и можно потреблять до или после того, как была вызвана MAPIInitialize. Возвращает успех или сбой с помощью стандартного HRESULT com и назначает параметр out экземпляру IMAPIInitMonitor.
  
## <a name="quick-info"></a>Краткие сведения

| идентификатор | result |
|:-----|:-----|
|Экспортируемая по:  <br/> |olmapi32.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |

## <a name="parameters"></a>Parameters
  
 _ppInitMonitor_
> [вышел] Указатель для получения вновь созданного экземпляра монитора инициализации MAPI.
  
## <a name="return-values"></a>Возвращаемые значения

S_OK
> Успешно создан новый экземпляр монитора инициализации.

E_OUTOFMEMORY
> Не хватило памяти, чтобы обустраить новый объект.

## <a name="see-also"></a>См. также
[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
