---
title: Руководство по RDS (Visual J++)
TOCTitle: RDS Tutorial (Visual J++)
ms:assetid: b5679bfe-e830-05df-8a1c-0744c96abe90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249870(v=office.15)
ms:contentKeyID: 48547248
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b01809cd17c9c1a5c1a73a5765bb8808692e4c2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877921"
---
# <a name="rds-tutorial-visual-j"></a>Руководство по RDS (Visual J++)


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

