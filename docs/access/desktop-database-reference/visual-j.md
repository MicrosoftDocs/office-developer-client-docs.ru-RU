---
title: Visual J ++ (Справочник по для настольных баз данных Access)
TOCTitle: Visual J++
ms:assetid: 5c05db85-cdf2-9a73-fbc5-3dbfa6752376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249320(v=office.15)
ms:contentKeyID: 48545079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3bc76026fb5b5b426b41c8334bc61d5b9485dd76
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481391"
---
# <a name="visual-j"></a><span data-ttu-id="edf51-102">Visual J++</span><span class="sxs-lookup"><span data-stu-id="edf51-102">Visual J++</span></span>


<span data-ttu-id="edf51-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="edf51-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="edf51-104">Этот короткий Microsoft Visual J ++ пример как собственную функцию можно связать с конкретным событием.</span><span class="sxs-lookup"><span data-stu-id="edf51-104">This short Microsoft Visual J++ example shows how you can associate your own function with a particular event.</span></span>

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

<span data-ttu-id="edf51-105">Во-первых, метод класса *onConnectionComplete* связан с событием **ConnectionComplete** , создав новый объект **ConnectionEventHandler** и назначение функции *onConnectComplete* объект.</span><span class="sxs-lookup"><span data-stu-id="edf51-105">First, the class method *onConnectionComplete* is associated with the **ConnectionComplete** event by creating a new **ConnectionEventHandler** object and assigning the *onConnectComplete* function to the object.</span></span>

<span data-ttu-id="edf51-106">*Основная* функция затем создает объект **подключения** и включает обработки путем вызова метода **addOnConnectComplete** и передачи его адрес функции *обработчика* событий.</span><span class="sxs-lookup"><span data-stu-id="edf51-106">The *main* function then creates a **Connection** object and enables event handling by calling the **addOnConnectComplete** method and passing it the address of the *handler* function.</span></span>

