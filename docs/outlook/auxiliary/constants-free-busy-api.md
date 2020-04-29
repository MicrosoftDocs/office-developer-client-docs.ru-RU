---
title: Константы (API сведений о доступности)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: В этом разделе содержатся определения констант, идентификаторы классов и идентификаторы интерфейсов для API сведений о доступности.
ms.openlocfilehash: 13578617eaab45e7194d7a0d4d6995ef925e7f20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431535"
---
# <a name="constants-freebusy-api"></a>Константы (API сведений о доступности)

В этом разделе содержатся определения констант, идентификаторы классов и идентификаторы интерфейсов для API сведений о доступности.
  
## <a name="constants"></a>Константы

|**Константа**|**Определение**|
|:-----|:-----|
|E_NOTIMPL  <br/> | *Как определено в файле заголовков пакета средств разработки программного обеспечения (SDK) для Microsoft Windows (SDK) Winerror. h.*  <br/> |
|E_OUTOFMEMORY  <br/> | *Как указано в файле заголовка пакета SDK для Windows, как указано в файле Winerror. h.*  <br/> |
|S_FALSE  <br/> | *Как указано в файле заголовка пакета SDK для Windows, как указано в файле Winerror. h.*  <br/> |
|S_OK  <br/> | *Как указано в файле заголовка пакета SDK для Windows, как указано в файле Winerror. h.*  <br/> |
   
## <a name="interface-identifiers"></a>Идентификаторы интерфейсов

Для следующих идентификаторов интерфейса следует предполагать DEFINE_GUID макрос, определенный в файле заголовка Windows SDK guiddef. h, чтобы связать символьное имя GUID со значением.
  
{00067064-0000-0000 — C000 — 000000000046}
  
DEFINE_GUID (IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  
{00067066-0000-0000 — C000 — 000000000046}
  
DEFINE_GUID (IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  
{00067067-0000-0000 — C000 — 000000000046}
  
DEFINE_GUID (IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  

