---
title: Constants (Free/busy API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: В этом разделе содержатся определения констант, идентификаторы классов и идентификаторы интерфейса для API занятости.
ms.openlocfilehash: 13578617eaab45e7194d7a0d4d6995ef925e7f20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431535"
---
# <a name="constants-freebusy-api"></a>Constants (Free/busy API)

В этом разделе содержатся определения констант, идентификаторы классов и идентификаторы интерфейса для API занятости.
  
## <a name="constants"></a>Константы

|**Константа**|**Определение**|
|:-----|:-----|
|E_NOTIMPL  <br/> | *Как определено в файле заглавного файла winerror.h комплекта средств разработки программного обеспечения для Microsoft Windows (SDK).*  <br/> |
|E_OUTOFMEMORY  <br/> | *Как определено в файле загона Windows SDK winerror.h.*  <br/> |
|S_FALSE  <br/> | *Как определено в файле загона Windows SDK winerror.h.*  <br/> |
|S_OK  <br/> | *Как определено в файле загона Windows SDK winerror.h.*  <br/> |
   
## <a name="interface-identifiers"></a>Идентификаторы интерфейсов

Для следующих идентификаторов интерфейса предположим, что макрос DEFINE_GUID, определенный в файле guiddef.h файла заголовки Windows SDK, чтобы связать символьное имя GUID с его значением.
  
{00067064-0000-0000-C000-000000000046}
  
DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  
{00067066-0000-0000-C000-000000000046}
  
DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  
{00067067-0000-0000-C000-000000000046}
  
DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  

