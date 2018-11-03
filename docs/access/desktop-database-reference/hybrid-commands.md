---
title: Гибридные команды (Справочник по для настольных баз данных Access)
TOCTitle: Hybrid commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 046d005eb4a9e1c8097908e0104b8d1e5c76e2af
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946917"
---
# <a name="hybrid-commands"></a>Гибридные команд


**Применимо к**: Access 2013, Office 2013

Гибридные команды, частично параметризованные команды. Пример:

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

Поведение кэширования для гибридных команды — это же, что регулярное параметризованные команды.

