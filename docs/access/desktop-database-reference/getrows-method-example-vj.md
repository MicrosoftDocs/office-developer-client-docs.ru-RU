---
title: Пример использования метода GetRows (VJ++)
TOCTitle: GetRows method example (VJ++)
ms:assetid: 60f7d621-3a9d-167e-8798-aeb2a881d975
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249355(v=office.15)
ms:contentKeyID: 48545194
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 06803c1a37f848580025103914838d59f0b5f59a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292211"
---
# <a name="getrows-method-example-vj"></a><span data-ttu-id="1d96b-102">Пример использования метода GetRows (VJ++)</span><span class="sxs-lookup"><span data-stu-id="1d96b-102">GetRows method example (VJ++)</span></span>


<span data-ttu-id="1d96b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d96b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d96b-104">В этом примере метод [GetRows](getrows-method-ado.md) используется для получения указанного количества строк из объекта [Recordset](recordset-object-ado.md) и заполнения массива полученными данными.</span><span class="sxs-lookup"><span data-stu-id="1d96b-104">This example uses the [GetRows](getrows-method-ado.md) method to retrieve a specified number of rows from a [Recordset](recordset-object-ado.md) and to fill an array with the resulting data.</span></span> <span data-ttu-id="1d96b-105">Метод **GetRows** будет возвращать меньше требуемого количества строк в двух случаях: либо при достижении [конца файла](bof-eof-properties-ado.md) , либо при попытке получить \*\*\*\* запись, которая была удалена другим пользователем.</span><span class="sxs-lookup"><span data-stu-id="1d96b-105">The **GetRows** method will return less than the desired number of rows in two cases: either if [EOF](bof-eof-properties-ado.md) has been reached, or if **GetRows** tried to retrieve a record that was deleted by another user.</span></span> <span data-ttu-id="1d96b-106">Функция возвращает **значение false** только в том случае, если происходит второй вариант.</span><span class="sxs-lookup"><span data-stu-id="1d96b-106">The function returns **False** only if the second case occurs.</span></span> <span data-ttu-id="1d96b-107">Для выполнения этой процедуры требуется функция Жетровсок.</span><span class="sxs-lookup"><span data-stu-id="1d96b-107">The GetRowsOK function is required for this procedure to run.</span></span>

```java 
 
// BeginGetRowsJ 
// The WFC class includes the ADO objects. 
 
import com.ms.wfc.data.*; 
import java.io.* ; 
import com.ms.com.*; 
 
public class GetRowsX 
{ 
 // The main entry point for the application. 
 
 static Variant avarRecords = null; 
 
 public static void main (String[] args) 
 { 
 GetRowsX(); 
 System.exit(0); 
 } 
 
 // GetRowsX function 
 
 static void GetRowsX() 
 { 
 
 // Define ADO Objects. 
 Recordset rstEmployees = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String line = null; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 int intRows; 
 int intRecord; 
 int intUBound; 
 int intDisplaysize = 15; 
 
 try 
 { 
 // Open recordset with names and hire dates from Employees table. 
 rstEmployees = new Recordset(); 
 rstEmployees.open("SELECT fName, lName, hire_date " + 
 "FROM Employee ORDER BY lName", strCnn, 
 AdoEnums.CursorType.FORWARDONLY, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TEXT); 
 
 while(true) 
 { 
 // Get user input for number of rows. 
 System.out.println( 
 "\nEnter number of rows to retrieve. (<= 0 to Exit)"); 
 line = in.readLine().trim(); 
 
 // Convert string entry to int. 
 intRows = Integer.parseInt(line); 
 
 // Exit the application if intRows is negative or zero. 
 if(intRows <= 0) 
 break; 
 
 // If GetRowsOK is successful, print the results, 
 // noting if the end of the file was reached. 
 if(GetRowsOK(rstEmployees,intRows)) 
 { 
 SafeArray sa = avarRecords.toSafeArray(); 
 intUBound = sa.getUBound(2); 
 if ( intRows > (intUBound + 1)) 
 System.out.println("\n(Not enough records in " + 
 "Recordset to retrieve " + intRows + " rows.)"); 
 System.out.println("\n" + (intUBound+ 1) + 
 " records found.\n"); 
 
 // Print the retrieved data. 
 
 for ( intRecord = sa.getLBound(); 
 intRecord <= intUBound; intRecord++) 
 { 
 
 System.out.println( 
 " " + sa.getString(0, intRecord) + " " + 
 sa.getString(1, intRecord) + ", " + 
 sa.getString(2, intRecord)); 
 if ( ((intRecord +1) % intDisplaysize) == 0) 
 { 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 
 } 
 } 
 else 
 { 
 // Assuming the GetRows error was due to data 
 // changes by another user, use Requery to 
 // refresh the Recordset and start over. 
 System.out.println("\nGetRows failed--retry? (Y/N)"); 
 if(in.readLine().trim().toUpperCase().equals("Y")) 
 rstEmployees.requery(); 
 else 
 { 
 System.out.println("GetRows failed!"); 
 break; 
 } 
 } 
 
 // Because using GetRows leaves the current 
 // record pointer at the last record accessed, 
 // move the pointer back to the beginning of the 
 // Recordset before looping back for another search. 
 rstEmployees.moveFirst(); 
 } 
 
 // Cleanup objects before exit. 
 rstEmployees.close(); 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
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
 
 // Display Error that the application has attempted to convert 
 // a string of inappropriate format to one of the numeric types. 
 catch(java.lang.NumberFormatException ne) 
 { 
 System.out.println( 
 "Exception: Must specify an Integer value." ); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstEmployees != null) 
 if (rstEmployees.getState() == 1) 
 rstEmployees.close(); 
 } 
 
 } 
 
 // GetRowsOK Function 
 
 static boolean GetRowsOK(Recordset rstTemp,int intNumber) 
 { 
 // Store results of GetRows method in array. 
 avarRecords = rstTemp.getRows(intNumber); 
 
 // Return False only if fewer than the desired 
 // number of rows were returned, but not because the 
 // end of the Recordset was reached. 
 if ( intNumber > (avarRecords.toSafeArray().getUBound(2)+ 1) 
 && !(rstTemp.getEOF())) 
 return false; 
 else 
 return true; 
 
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
// EndGetRowsJ 
```

