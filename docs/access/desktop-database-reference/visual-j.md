---
title: Visual J++ (Справочник по базам данных Access для настольных ПК)
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
# <a name="visual-j"></a>Visual J++


**Область применения**: Access 2013, Office 2013

В этом кратком примере для Microsoft Visual J++ показано, как связать свою функцию с определенным событием.

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

Во-первых, метод класса *онконнектионкомплете* связан с событием **коннектионкомплете** путем создания нового объекта **коннектионевенсандлер** и назначения функции *онконнекткомплете* объекту.

Затем функция *Main* создает объект **Connection** и включает обработку событий, вызывая метод **аддонконнекткомплете** и передавая ему адрес функции обработчика. **

