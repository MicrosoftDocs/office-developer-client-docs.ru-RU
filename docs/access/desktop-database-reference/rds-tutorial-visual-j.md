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
# <a name="rds-tutorial-visual-j"></a><span data-ttu-id="3ff5c-102">При помощи учебника по служб удаленных рабочих СТОЛОВ (Visual J ++)</span><span class="sxs-lookup"><span data-stu-id="3ff5c-102">RDS tutorial (Visual J++)</span></span>


<span data-ttu-id="3ff5c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ff5c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ff5c-104">ADO/WFC не соответствующего полностью объектной модели служб удаленных рабочих СТОЛОВ, то есть не реализует [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="3ff5c-104">ADO/WFC does not completely follow the RDS object model in that it does not implement the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="3ff5c-105">ADO/WFC только реализует класс со стороны клиента, [RDS. Пространства данных](dataspace-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="3ff5c-105">ADO/WFC only implements the client-side class, [RDS.DataSpace](dataspace-object-rds.md).</span></span>

<span data-ttu-id="3ff5c-106">Класс **пространства данных** реализует один метод [CreateObject](createobject-method-rds.md), которое возвращает объект [ObjectProxy](https://msdn.microsoft.com/library/jj249624\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="3ff5c-106">The **DataSpace** class implements one method, [CreateObject](createobject-method-rds.md), which returns an [ObjectProxy](https://msdn.microsoft.com/library/jj249624\(v=office.15\)) object.</span></span> <span data-ttu-id="3ff5c-107">Класс **пространства данных** также внедряет свойство [InternetTimeout](internettimeout-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="3ff5c-107">The **DataSpace** class also implements the [InternetTimeout](internettimeout-property-rds.md) property.</span></span>

<span data-ttu-id="3ff5c-108">Класс **ObjectProxy** реализует один метод, позвонить, которой можно было вызвать любой объект бизнеса на сервере.</span><span class="sxs-lookup"><span data-stu-id="3ff5c-108">The **ObjectProxy** class implements one method, call, which can invoke any server-side business object.</span></span>

<span data-ttu-id="3ff5c-109">**Это начало учебника по.**</span><span class="sxs-lookup"><span data-stu-id="3ff5c-109">**This is the beginning of the tutorial.**</span></span>

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

<span data-ttu-id="3ff5c-110">**Это конце обучения.**</span><span class="sxs-lookup"><span data-stu-id="3ff5c-110">**This is the end of the tutorial.**</span></span>

