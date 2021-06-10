---
title: Пример использования свойств CursorType, LockType и EditMode (VJ++)
TOCTitle: CursorType, LockType, and EditMode properties example (VJ++)
ms:assetid: bfe87584-4909-8974-b207-4a0c363c5155
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249932(v=office.15)
ms:contentKeyID: 48547497
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4bdf0ee11a90348752a29c5a8ecf059a8ebe98d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295193"
---
# <a name="cursortype-locktype-and-editmode-properties-example-vj"></a><span data-ttu-id="af9ba-102">Пример использования свойств CursorType, LockType и EditMode (VJ++)</span><span class="sxs-lookup"><span data-stu-id="af9ba-102">CursorType, LockType, and EditMode properties example (VJ++)</span></span>


<span data-ttu-id="af9ba-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="af9ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="af9ba-104">В этом примере показано, как установить свойства [CursorType](cursortype-property-ado.md) и [LockType](locktype-property-ado.md) перед открытием [наборов записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="af9ba-104">This example demonstrates setting the [CursorType](cursortype-property-ado.md) and [LockType](locktype-property-ado.md) properties before opening a [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="af9ba-105">В нем также показано значение свойства [EditMode](editmode-property-ado.md) в различных условиях.</span><span class="sxs-lookup"><span data-stu-id="af9ba-105">It also shows the value of the [EditMode](editmode-property-ado.md) property under various conditions.</span></span> <span data-ttu-id="af9ba-106">Для запуска этой процедуры требуется функция EditModeOutput.</span><span class="sxs-lookup"><span data-stu-id="af9ba-106">The EditModeOutput function is required for this procedure to run.</span></span>

```java 
 
// BeginEditModeJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class EditModeX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 EditModeX (); 
 System.exit(0); 
 } 
 
 // EditModeX function 
 
 static void EditModeX () 
 { 
 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Recordset rstEmployees = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String line = null; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 try 
 { 
 // Open recordset with data from Employees table. 
 
 cnConn1 = new Connection(); 
 cnConn1.open(strCnn); 
 rstEmployees = new Recordset(); 
 rstEmployees.setActiveConnection(cnConn1); 
 rstEmployees.setCursorLocation(AdoEnums.CursorLocation.CLIENT); 
 rstEmployees.setCursorType(AdoEnums.CursorType.STATIC); 
 rstEmployees.setLockType(AdoEnums.LockType.BATCHOPTIMISTIC); 
 rstEmployees.open("employee", cnConn1, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.BATCHOPTIMISTIC, 
 AdoEnums.CommandType.TABLE); 
 
 // Show the EditMode property under different editing states. 
 
 rstEmployees.addNew(); 
 rstEmployees.getField("emp_id").setString("T-T55555M"); 
 rstEmployees.getField("fname").setString("temp_fname"); 
 rstEmployees.getField("lname").setString("temp_lname"); 
 EditModeOutput("After AddNew:", rstEmployees.getEditMode()); 
 rstEmployees.updateBatch(); 
 EditModeOutput("After Update:", rstEmployees.getEditMode()); 
 rstEmployees.getField("fname").setString("test"); 
 EditModeOutput("After Edit:", rstEmployees.getEditMode()); 
 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 // Delete new record because this is a demonstration. 
 cnConn1.execute( 
 "DELETE FROM employee WHERE emp_id = 'T-T55555M'"); 
 
 // Cleanup objects before exit. 
 rstEmployees.close(); 
 cnConn1.close(); 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // Check for null pointer for connection object. 
 if (cnConn1==null) 
 System.out.println("Exception: " + ae.getMessage()); 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstEmployees != null) 
 { 
 PrintProviderError(rstEmployees.getActiveConnection()); 
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
 if (rstEmployees != null) 
 if (rstEmployees.getState() == 1) 
 rstEmployees.close(); 
 } 
 } 
 
 // EditModeOutput Function 
 
 static void EditModeOutput(String strTemp, int intEditMode) 
 { 
 String strMessage=""; 
 // Print report based on the value of the EditMode 
 // property. 
 
 System.out.println("\n" + strTemp); 
 strMessage ="\n\tEditMode = "; 
 switch(intEditMode) 
 { 
 case AdoEnums.EditMode.NONE : 
 strMessage+="adEditNone"; 
 break; 
 case AdoEnums.EditMode.INPROGRESS : 
 strMessage+="adEditInProgress"; 
 break; 
 case AdoEnums.EditMode.ADD : 
 strMessage+="adEditAdd"; 
 break; 
 default : 
 break; 
 } 
 System.out.println(strMessage); 
 } 
 
 // PrintProviderError Function 
 
 static void PrintProviderError( Connection Cnn1 ) 
 { 
 // Print Provider errors from Connection object. 
 // ErrItem is an item object in the Connections Errors collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = Cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if( nCount > 0); 
 { 
 // Collection ranges from 0 to nCount - 1 
 for (i = 0; i< nCount; i++) 
 { 
 ErrItem = Cnn1.getErrors().getItem(i); 
 System.out.println("\t Error number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription() ); 
 } 
 } 
 
 } 
 
 // PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
// EndEditModeJ 
```

