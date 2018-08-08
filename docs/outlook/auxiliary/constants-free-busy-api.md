---
title: Константы (занятости API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: В этом разделе содержатся определения констант, класс идентификаторы и идентификаторы интерфейса для API свободен/занят.
ms.openlocfilehash: ec909d449dc9075959fc9c047457577efd52ec3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807686"
---
# <a name="constants-freebusy-api"></a>Константы (занятости API)

В этом разделе содержатся определения констант, класс идентификаторы и идентификаторы интерфейса для API свободен/занят.
  
## <a name="constants"></a>Константы

|**Constant**|**Определение**|
|:-----|:-----|
|E_NOTIMPL  <br/> | *Определенные в файле winerror.h файл заголовка Microsoft Windows Software Development Kit (SDK).*  <br/> |
|E_OUTOFMEMORY  <br/> | *Определенные в файле winerror.h файл заголовка пакета SDK Windows.*  <br/> |
|S_FALSE  <br/> | *Определенные в файле winerror.h файл заголовка пакета SDK Windows.*  <br/> |
|ЗНАЧЕНИЕ S_OK  <br/> | *Определенные в файле winerror.h файл заголовка пакета SDK Windows.*  <br/> |
   
## <a name="interface-identifiers"></a>Идентификаторы интерфейса

Следующие идентификаторы интерфейса предполагается макрос DEFINE_GUID определенные в guiddef.h файл заголовка Windows SDK для связи символическое имя GUID с его значение.
  
{00067064-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IEnumFBBlock 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  
{00067066-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusyData 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  
{00067067-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusySupport 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  

