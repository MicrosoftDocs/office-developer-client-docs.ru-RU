---
title: RDS Tutorial (Visual J++)
TOCTitle: RDS Tutorial (Visual J++)
ms:assetid: b5679bfe-e830-05df-8a1c-0744c96abe90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249870(v=office.15)
ms:contentKeyID: 48547248
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 15eadc36079faa529585e539b67eb0da246cf4bc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481357"
---
# <a name="rds-tutorial-visual-j"></a><span data-ttu-id="bf295-102">RDS Tutorial (Visual J++)</span><span class="sxs-lookup"><span data-stu-id="bf295-102">RDS Tutorial (Visual J++)</span></span>


<span data-ttu-id="bf295-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf295-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bf295-104">ADO/WFC не соответствующего полностью объектной модели служб удаленных рабочих СТОЛОВ, то есть не реализует [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="bf295-104">ADO/WFC does not completely follow the RDS object model in that it does not implement the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="bf295-105">ADO/WFC только реализует класс со стороны клиента, [RDS. Пространства данных](dataspace-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="bf295-105">ADO/WFC only implements the client-side class, [RDS.DataSpace](dataspace-object-rds.md).</span></span>

<span data-ttu-id="bf295-106">Класс **пространства данных** реализует один метод [CreateObject](createobject-method-rds.md), которое возвращает объект [ObjectProxy](https://msdn.microsoft.com/library/jj249624\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="bf295-106">The **DataSpace** class implements one method, [CreateObject](createobject-method-rds.md), which returns an [ObjectProxy](https://msdn.microsoft.com/library/jj249624\(v=office.15\)) object.</span></span> <span data-ttu-id="bf295-107">Класс **пространства данных** также внедряет свойство [InternetTimeout](internettimeout-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="bf295-107">The **DataSpace** class also implements the [InternetTimeout](internettimeout-property-rds.md) property.</span></span>

<span data-ttu-id="bf295-108">Класс **ObjectProxy** реализует один метод, позвонить, которой можно было вызвать любой объект бизнеса на сервере.</span><span class="sxs-lookup"><span data-stu-id="bf295-108">The **ObjectProxy** class implements one method, call, which can invoke any server-side business object.</span></span>

<span data-ttu-id="bf295-109">**Это начало учебника по.**</span><span class="sxs-lookup"><span data-stu-id="bf295-109">**This is the beginning of the tutorial.**</span></span>

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

<span data-ttu-id="bf295-110">**Это конце обучения.**</span><span class="sxs-lookup"><span data-stu-id="bf295-110">**This is the end of the tutorial.**</span></span>

