---
title: Пример использования методов Execute, Requery и Clear (VJ++)
TOCTitle: Execute, Requery, and Clear methods example (VJ++)
ms:assetid: 00210f2e-7454-25c7-a035-68344868fe11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248774(v=office.15)
ms:contentKeyID: 48542897
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4701e390a26fa8a29bf7e7fa490f188f80820876
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862529"
---
# <a name="execute-requery-and-clear-methods-example-vj"></a>Пример использования методов Execute, Requery и Clear (VJ++)


**Применимо к**: Access 2013 | Office 2013

В этом примере демонстрируется использование метода **Execute** при вызове из объекта [команды](command-object-ado.md) и объект [подключения](connection-object-ado.md) . Он также использует метод [повторный запрос](requery-method-ado.md) для получения текущих данных в наборе записей и метод [снимите флажок](clear-method-ado.md) , чтобы удалить содержимое семейства [Errors](errors-collection-ado.md) . Процедуры ExecuteCommand и PrintOutput необходимы для выполнения этой процедуры.

```java 
 
// BeginExecuteJ 
// The WFC class includes the ADO objects. 
import com.ms.wfc.data.*; 
import java.io.*; 
 
public class ExecuteX 
{ 
 // Main Function 
 
 public static void main (String[] args) 
 { 
 ExecuteX(); 
 } 
 
 // ExecuteX Function 
 
 static void ExecuteX() 
 { 
 // Define string variables. 
 String strSQLChange = "UPDATE Titles SET Type = " 
 + "'self_help' WHERE Type = 'psychology'"; 
 String strSQLRestore = "UPDATE Titles SET Type = " 
 + "'psychology' WHERE Type = 'self_help'"; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 // Define ADO objects. 
 Connection cnConn1 = null; 
 Command cmdChange = null; 
 Recordset rsTitles = null; 
 
 try 
 { 
 // Open connection. 
 cnConn1 = new Connection (); 
 cnConn1.open(strCnn, "", "", AdoEnums.CommandType.UNSPECIFIED); 
 
 // Create command object. 
 cmdChange = new Command(); 
 cmdChange.setActiveConnection (cnConn1); 
 cmdChange.setCommandText (strSQLChange); 
 
 // Open recordset with Titles table. 
 rsTitles = new Recordset(); 
 rsTitles.open("Titles", cnConn1, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.OPTIMISTIC, 
 AdoEnums.CommandType.TABLE); 
 
 // Print report of original data. 
 System.out.println("\n\n\tData in Titles table " 
 + "before executing the query: \n"); 
 PrintOutput(rsTitles); 
 
 // Clear extraneous errors from the Errors collection. 
 cnConn1.getErrors().clear(); 
 
 // Call the ExecuteCommand subroutine to 
 // execute cmdChange command. 
 ExecuteCommand(cmdChange, rsTitles); 
 
 // Print report of new data. 
 System.out.println("\n\n\tData in Titles table after " 
 + "executing the query: \n"); 
 PrintOutput(rsTitles); 
 
 // Use the Connection object's execute method to 
 // execute SQL statement to restore data. 
 cnConn1.execute(strSQLRestore); 
 
 // Print report of restored data. 
 System.out.println("\n\n\tData after executing the query " 
 + "to restore the original information: \n"); 
 PrintOutput(rsTitles); 
 } // End Try statement. 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rsTitles != null) 
 { 
 PrintProviderError(rsTitles.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rsTitles != null) 
 if (rsTitles.getState() == 1) 
 rsTitles.close(); 
 if (cnConn1 != null) 
 if (cnConn1.getState() == 1) 
 cnConn1.close(); 
 } 
 } 
 
 // ExecuteCommand Function 
 
 static void ExecuteCommand(Command cmdTemp, Recordset rstTemp) 
 { 
 try 
 { 
 // CommandText property already set before function was called. 
 cmdTemp.setCommandType(AdoEnums.CommandType.TEXT); 
 cmdTemp.execute(); 
 
 // Retrieve the current data by requerying the recordset. 
 rstTemp.requery(AdoEnums.CommandType.UNKNOWN); 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 PrintProviderError(rstTemp.getActiveConnection()); 
 } 
 } 
 
 // PrintOutput Function 
 
 static void PrintOutput(Recordset rstTemp) 
 { 
 // Declarations. 
 BufferedReader in = new 
 BufferedReader(new InputStreamReader(System.in)); 
 
 // Ensure at top of recordset. 
 rstTemp.moveFirst(); 
 
 // If EOF is true, then no data and skip print loop. 
 if( rstTemp.getEOF() ) 
 { 
 System.out.println("\tRecordset empty\n"); 
 } 
 else 
 { 
 // Enumerate Recordset and print data from each. 
 while( !(rstTemp.getEOF()) ) 
 { 
 // Convert variant string to convertable string type. 
 System.out.println("\t" 
 + rstTemp.getFields().getItem("Title").getValue() + " " 
 + rstTemp.getFields().getItem("Type").getValue() + "\n"); 
 rstTemp.moveNext(); 
 } 
 } 
 try 
 { 
 System.out.println("\nPress <Enter> key to continue."); 
 in.readLine(); 
 } 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
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
// EndExecuteJ 
```

