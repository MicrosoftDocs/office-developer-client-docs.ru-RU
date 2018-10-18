---
<span data-ttu-id="058c3-101"><<<<<<< Название HEAD: пример свойства Value (VJ ++) TOCTitle: пример свойства Value (VJ ++) === название: пример свойства Value (VJ ++) TOCTitle: пример свойства Value (VJ ++)</span><span class="sxs-lookup"><span data-stu-id="058c3-101"><<<<<<< HEAD title: Value Property Example (VJ++) TOCTitle: Value Property Example (VJ++) ======= title: Value property example (VJ++) TOCTitle: Value property example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="058c3-102">главные ms:assetid: 1894c483-f5b0-c83e-35fb-c975ca867fc9 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248934(v=office.15) ms:contentKeyID: 48543474 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="058c3-102">master ms:assetid: 1894c483-f5b0-c83e-35fb-c975ca867fc9 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248934(v=office.15) ms:contentKeyID: 48543474 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="058c3-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="058c3-103"><<<<<<< HEAD</span></span>
# <a name="value-property-example-vj"></a><span data-ttu-id="058c3-104">Value Property Example (VJ++)</span><span class="sxs-lookup"><span data-stu-id="058c3-104">Value Property Example (VJ++)</span></span>
=======
# <a name="value-property-example-vj"></a><span data-ttu-id="058c3-105">Пример свойства Value (VJ ++)</span><span class="sxs-lookup"><span data-stu-id="058c3-105">Value property example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="058c3-106">master</span><span class="sxs-lookup"><span data-stu-id="058c3-106">master</span></span>


<span data-ttu-id="058c3-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="058c3-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="058c3-108">В этом примере показано [значение](value-property-ado.md) свойства с помощью [поля](field-object-ado.md) и [Свойства](property-object-ado.md) объектов, отображая поля и значения свойств для таблицы ***сотрудников*** .</span><span class="sxs-lookup"><span data-stu-id="058c3-108">This example demonstrates the [Value](value-property-ado.md) property with [Field](field-object-ado.md) and [Property](property-object-ado.md) objects by displaying field and property values for the ***Employees*** table.</span></span>

```java 
 
// BeginValueJ 
import java.io.*; 
import com.ms.wfc.data.*; 
import com.ms.com.*; 
 
public class ValueX 
{ 
 // Main Function 
 public static void main (String[] args) 
 { 
 ValueX(); 
 System.exit(0); 
 } 
 static void ValueX() 
 { 
 // Define ADO Objects. 
 Recordset rstEmployees = null; 
 Field fldLoop = null; 
 AdoProperty prpLoop = null; 
 
 // Declarations. 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 int intLoop; 
 BufferedReader in = new 
 BufferedReader(new InputStreamReader(System.in)); 
 Variant varPropertyValue; 
 String strMessage; 
 
 try 
 { 
 // Open a Recordset with data from Employees table. 
 rstEmployees = new Recordset(); 
 rstEmployees.open("employee", strCnn, 
 AdoEnums.CursorType.FORWARDONLY, AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TABLE); 
 
 System.out.println("Field values in rstEmployees\n"); 
 
 // Enumerate the Fields collection of the Employees 
 // table. 
 for(intLoop = 0; 
 intLoop<rstEmployees.getFields().getCount();intLoop++) 
 { 
 fldLoop = rstEmployees.getFields().getItem(intLoop); 
 // Because Value is the default property of a 
 // Field object, the use of the actual keyword 
 // here is optional. 
 System.out.println("\t" + fldLoop.getName() + " = " + 
 fldLoop.getValue()); 
 } 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 System.out.println("Property values in rstEmployees\n"); 
 
 // Enumerate the Properties collection of the 
 // Recordset object. 
 int intCount = 0; 
 for(intLoop = 0; 
 intLoop<rstEmployees.getProperties().getCount();intLoop++) 
 { 
 prpLoop = rstEmployees.getProperties().getItem(intLoop); 
 // Because Value is the default property of a 
 // Field object, the use of the actual keyword 
 // here is optional. 
 strMessage = "\t" + prpLoop.getName() + " = "; 
 varPropertyValue = prpLoop.getValue(); 
 short vttype =varPropertyValue.getvt(); 
 switch (vttype) 
 { 
 case Variant.VariantBoolean : 
 { 
 if (varPropertyValue.getBoolean()) 
 strMessage +="True"; 
 else 
 strMessage +="False"; 
 } 
 break; 
 case Variant.VariantInt : 
 strMessage += varPropertyValue.getInt(); 
 break; 
 default : 
 break; 
 } 
 System.out.println(strMessage); 
 intCount++; 
 // Loop used to display records 
 if (intCount % 15 == 0) 
 { 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 intCount = 0; 
 } 
 
 } 
 // Cleanup objects before exit. 
 rstEmployees.close(); 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 // System read requires this catch. 
 catch(java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 catch(AdoException ae) 
 { 
 // Notify the user of any errors that result from ADO. 
 
 // As passing a recordset, check for null pointer first. 
 if(rstEmployees != null) 
 { 
 PrintProviderError(rstEmployees.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstEmployees != null) 
 if (rstEmployees.getState() == 1) 
 rstEmployees.close(); 
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
// EndValueJ 
```

