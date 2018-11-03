---
title: При помощи учебника по служб удаленных рабочих СТОЛОВ (Visual J ++)
TOCTitle: RDS tutorial (Visual J++)
ms:assetid: b5679bfe-e830-05df-8a1c-0744c96abe90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249870(v=office.15)
ms:contentKeyID: 48547248
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e23af46ac7aab267eb5788aa4790d5c568f23609
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946127"
---
# <a name="rds-tutorial-visual-j"></a>При помощи учебника по служб удаленных рабочих СТОЛОВ (Visual J ++)


**Применимо к**: Access 2013, Office 2013

ADO/WFC не соответствующего полностью объектной модели служб удаленных рабочих СТОЛОВ, то есть не реализует [RDS. DataControl](datacontrol-object-rds.md) объекта. ADO/WFC только реализует класс со стороны клиента, [RDS. Пространства данных](dataspace-object-rds.md).

Класс **пространства данных** реализует один метод [CreateObject](createobject-method-rds.md), которое возвращает объект [ObjectProxy](https://msdn.microsoft.com/library/jj249624\(v=office.15\)) . Класс **пространства данных** также внедряет свойство [InternetTimeout](internettimeout-property-rds.md) .

Класс **ObjectProxy** реализует один метод, позвонить, которой можно было вызвать любой объект бизнеса на сервере.

**Это начало учебника по.**

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```

**Это конце обучения.**

