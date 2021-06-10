---
title: Visual J++ (ссылка на настольные базы данных)
TOCTitle: Visual J++
ms:assetid: 5c05db85-cdf2-9a73-fbc5-3dbfa6752376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249320(v=office.15)
ms:contentKeyID: 48545079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: da13ae0f10e2338b961f2f12686bd378580a69d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311335"
---
# <a name="visual-j"></a><span data-ttu-id="21211-102">Visual J++</span><span class="sxs-lookup"><span data-stu-id="21211-102">Visual J++</span></span>


<span data-ttu-id="21211-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21211-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21211-104">В этом кратком примере Microsoft Visual J++ показано, как можно связать свою функцию с определенным событием.</span><span class="sxs-lookup"><span data-stu-id="21211-104">This short Microsoft Visual J++ example shows how you can associate your own function with a particular event.</span></span>

```java 
 
// BeginEventExampleVJ 
import com.ms.wfc.data.*; 
 
public class EventExampleVJ 
{ 
 ConnectionEventHandler handler = new ConnectionEventHandler(this,"onConnectComplete"); 
 
 public void onConnectComplete(Object sender,ConnectionEvent e) 
 { 
 if (e.adStatus == AdoEnums.EventStatus.ERRORSOCCURRED) 
 System.out.println("Connection failed"); 
 else 
 System.out.println("Connection completed"); 
 return; 
 } 
 
 public static void main (String[] args) 
 { 
 EventExampleVJ Class1 = new EventExampleVJ(); 
 Connection conn = new Connection(); 
 
 conn.addOnConnectComplete(Class1.handler); // Enable event support. 
 conn.open("DSN=Pubs"); 
 conn.close(); 
 conn.removeOnConnectComplete(Class1.handler); // Disable event support. 
 } 
} 
// EndEventExampleVJ 
```

<span data-ttu-id="21211-105">Во-первых, метод класса *onConnectionComplete* связан с событием **ConnectionComplete,** создав новый объект **ConnectionEventHandler** и назначив объекту функцию *onConnectComplete.*</span><span class="sxs-lookup"><span data-stu-id="21211-105">First, the class method *onConnectionComplete* is associated with the **ConnectionComplete** event by creating a new **ConnectionEventHandler** object and assigning the *onConnectComplete* function to the object.</span></span>

<span data-ttu-id="21211-106">Затем *основная* функция создает объект **Connection** и включает обработку событий, вызывая метод **addOnConnectComplete** и передав ему адрес функции *обработчик.*</span><span class="sxs-lookup"><span data-stu-id="21211-106">The *main* function then creates a **Connection** object and enables event handling by calling the **addOnConnectComplete** method and passing it the address of the *handler* function.</span></span>

