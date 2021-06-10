---
title: Пример использования свойства StayInSync (VJ++)
TOCTitle: StayInSync property example (VJ++)
ms:assetid: e9e0fcc7-07b6-c433-7c4c-478fc69eacaf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250184(v=office.15)
ms:contentKeyID: 48548448
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0002f571a2022a7975271c40e9204864824bdb92
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314492"
---
# <a name="stayinsync-property-example-vj"></a><span data-ttu-id="43202-102">Пример использования свойства StayInSync (VJ++)</span><span class="sxs-lookup"><span data-stu-id="43202-102">StayInSync property example (VJ++)</span></span>


<span data-ttu-id="43202-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="43202-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="43202-104">В этом примере показано, как [свойство StayInSync](stayinsync-property-ado.md) облегчает доступ к строкам в иерархическом [наборе записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="43202-104">This example demonstrates how the [StayInSync](stayinsync-property-ado.md) property facilitates accessing rows in a hierarchical [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="43202-105">Внешний цикл отображает имя и фамилию каждого автора, состояние и идентификацию.</span><span class="sxs-lookup"><span data-stu-id="43202-105">The outer loop displays each author's first and last name, state, and identification.</span></span> <span data-ttu-id="43202-106">Приложение **Recordset** для каждой строки извлекается из коллекции [Fields](fields-collection-ado.md) и автоматически назначено свойству **StayInSync** **свойством rstTitleAuthor** всякий раз, когда родительский набор **записей** перемещается в новую строку.</span><span class="sxs-lookup"><span data-stu-id="43202-106">The appended **Recordset** for each row is retrieved from the [Fields](fields-collection-ado.md) collection and automatically assigned to **rstTitleAuthor** by the **StayInSync** property whenever the parent **Recordset** moves to a new row.</span></span> <span data-ttu-id="43202-107">Внутренний цикл отображает четыре поля из каждой строки в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="43202-107">The inner loop displays four fields from each row in the appended recordset.</span></span>

```java 
 
// BeginStayInSyncJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
import com.ms.com.*; 
 
public class StayInSyncX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 StayInSyncX(); 
 System.exit(0); 
 } 
 
 // StayInSyncX function 
 
 static void StayInSyncX() 
 { 
 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Recordset rstAuthors = null; 
 Recordset rstTitleAuthor = null; 
 
 // Declarations. 
 BufferedReader in = new 
 BufferedReader (new InputStreamReader(System.in)); 
 String strCnn = "Provider=MSDataShape;" + 
 "Data Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 
 try 
 { 
 cnConn1 = new Connection(); 
 cnConn1.open(strCnn); 
 rstAuthors = new Recordset(); 
 rstAuthors.setStayInSync(true); 
 rstAuthors.open("SHAPE {select * from Authors} " + 
 "APPEND ({select * from titleauthor}" + 
 "RELATE au_id TO au_id) AS chapTitleAuthor", 
 cnConn1, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TEXT); 
 
 Variant varRstTitleAuthor = rstAuthors.getFields(). 
 getItem("chapTitleAuthor").getValue(); 
 rstTitleAuthor =new Recordset(varRstTitleAuthor.toObject()); 
 int intCount =0; 
 while(!rstAuthors.getEOF()) 
 { 
 System.out.println("\n" + 
 rstAuthors.getField("au_fname").getString() + " " + 
 rstAuthors.getField("au_lname").getString() + " " + 
 rstAuthors.getField("state").getString() + " " + 
 rstAuthors.getField("au_id").getString()); 
 while(!rstTitleAuthor.getEOF()) 
 { 
 System.out.println(rstTitleAuthor.getField(0). 
 getString() + " " + 
 rstTitleAuthor.getField(1).getString() + " " + 
 rstTitleAuthor.getField(2).getString() + " " + 
 rstTitleAuthor.getField(3).getString()); 
 rstTitleAuthor.moveNext(); 
 } 
 if(++intCount % 5 == 0) 
 { 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 rstAuthors.moveNext(); 
 } 
 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstAuthors != null) 
 { 
 PrintProviderError(rstAuthors.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstTitleAuthor != null) 
 if (rstTitleAuthor.getState() == 1) 
 rstTitleAuthor.close(); 
 if (rstAuthors != null) 
 if (rstAuthors.getState() == 1) 
 rstAuthors.close(); 
 if (cnConn1 != null) 
 if (cnConn1.getState() == 1) 
 cnConn1.close(); 
 } 
 } 
 
 // PrintProviderError Function 
 static void PrintProviderError(Connection cnn1) 
 { 
 // Print Provider Errors from Connection Object. 
 // ErrItem is an item object in the Connections Errors Collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if ( nCount > 0) 
 { 
 // Collection ranges from 0 to nCount-1. 
 for ( i=0;i<nCount; i++) 
 { 
 ErrItem = cnn1.getErrors().getItem(i); 
 System.out.println("\t Error Number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription()); 
 } 
 } 
 } 
 // PrintIOError Function 
 static void PrintIOError(java.io.IOException je) 
 { 
 System.out.println("Error: \n"); 
 System.out.println("\t Source: " + je.getClass() + "\n"); 
 System.out.println("\t Description: "+ je.getMessage() + "\n"); 
 } 
} 
// EndStayInSyncJ 
```

