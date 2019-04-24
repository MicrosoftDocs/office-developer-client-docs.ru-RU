---
title: Пример использования свойств ConnectionString, ConnectionTimeout и State (VJ++)
TOCTitle: ConnectionString, ConnectionTimeout, and State properties example (VJ++)
ms:assetid: 88b3f95e-0e46-7cbb-8086-d583319a6628
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249599(v=office.15)
ms:contentKeyID: 48546141
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 81d4fa54d966d04e17ccbdadee52303f857c024b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295725"
---
# <a name="connectionstring-connectiontimeout-and-state-properties-example-vj"></a><span data-ttu-id="4298d-102">Пример использования свойств ConnectionString, ConnectionTimeout и State (VJ++)</span><span class="sxs-lookup"><span data-stu-id="4298d-102">ConnectionString, ConnectionTimeout, and State properties example (VJ++)</span></span>


<span data-ttu-id="4298d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4298d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4298d-104">В этом примере показаны различные способы использования свойства [ConnectionString](connectionstring-property-ado.md) для открытия объекта [Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="4298d-104">This example demonstrates different ways of using the [ConnectionString](connectionstring-property-ado.md) property to open a [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="4298d-105">Кроме того, используется свойство [ConnectionTimeout](connectiontimeout-property-ado.md) для задания периода ожидания подключения и свойство [State](state-property-ado.md) для проверки состояния подключений.</span><span class="sxs-lookup"><span data-stu-id="4298d-105">It also uses the [ConnectionTimeout](connectiontimeout-property-ado.md) property to set a connection timeout period, and the [State](state-property-ado.md) property to check the state of the connections.</span></span> <span data-ttu-id="4298d-106">Для выполнения этой процедуры требуется функция-State.</span><span class="sxs-lookup"><span data-stu-id="4298d-106">The GetState function is required for this procedure to run.</span></span>

```java 
 
// BeginConnectionStringJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class ConnectionStringX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 ConnectionStringX(); 
 System.exit(0); 
 } 
 
 // ConnectionStringX function 
 
 static void ConnectionStringX() 
 { 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Connection cnConn2 = null; 
 Connection cnConn3 = null; 
 Connection cnConn4 = null; 
 
 //Declarations. 
 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String line = null; 
 String strTemp; 
 
 try 
 { 
 // Open a connection using OLE DB syntax. 
 cnConn1 = new Connection(); 
 cnConn1.setConnectionString( 
 "Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"); 
 cnConn1.setCommandTimeout(30); 
 cnConn1.open(); 
 strTemp = getState(cnConn1.getState()); 
 System.out.println("CnConn1 state: " + strTemp); 
 
 // Open a connection using a DSN and ODBC tags. 
 // It is assumed that you have create DSN 'Pubs' with a user name as 
 // 'MyUserId' and password as 'MyPassword'. 
 cnConn2 = new Connection(); 
 cnConn2.setConnectionString("DSN='Pubs';UID='MyUserId';PWD='MyPassword';"); 
 cnConn2.open(); 
 strTemp = getState(cnConn2.getState()); 
 System.out.println("CnConn2 state: " + strTemp); 
 
 // Open a connection using a DSN and OLE DB tags. 
 cnConn3 = new Connection(); 
 cnConn3.setConnectionString 
 ("Data Source='Pubs';"); 
 cnConn3.open(); 
 strTemp = getState(cnConn3.getState()); 
 System.out.println("CnConn3 state: " + strTemp); 
 
 // Open a connection using a DSN and individual 
 // arguments instead of a connection string. 
 // It is assumed that you have create DSN 'Pubs' with a user name as 
 // 'MyUserId' and password as 'MyPassword'. 
 cnConn4 = new Connection(); 
 cnConn4.open("Pubs", "MyUserId", "MyPassword"); 
 strTemp = getState(cnConn4.getState()); 
 System.out.println("CnConn4 state: " + strTemp); 
 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 System.out.println("Exception: " + ae.getMessage()); 
 
 } 
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (cnConn1 != null) 
 if (cnConn1.getState() == 1) 
 cnConn1.close(); 
 if (cnConn2 != null) 
 if (cnConn2.getState() == 1) 
 cnConn2.close(); 
 if (cnConn3 != null) 
 if (cnConn3.getState() == 1) 
 cnConn3.close(); 
 if (cnConn4 != null) 
 if (cnConn4.getState() == 1) 
 cnConn4.close(); 
 } 
 
 } 
 
 // getState Function 
 
 static String getState(int intState) 
 { 
 // Returns current state of the connection object. 
 String strState=null; 
 
 switch(intState) 
 { 
 case AdoEnums.ObjectState.CLOSED : 
 strState = new String("adStateClosed"); 
 break; 
 case AdoEnums.ObjectState.OPEN : 
 strState = new String("adStateOpen"); 
 break; 
 default : 
 break; 
 } 
 return strState; 
 } 
 
 // PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
 
// EndConnectionStringJ 
```

