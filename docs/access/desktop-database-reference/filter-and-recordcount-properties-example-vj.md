---
<span data-ttu-id="08be5-101"><<<<<<< HEAD заголовок: фильтр и TOCTitle пример свойств RecordCount (VJ ++): фильтр и пример свойств RecordCount (VJ ++) === заголовок: пример свойств фильтра и RecordCount (VJ ++) TOCTitle: фильтр и RecordCount Пример: свойства (VJ ++)</span><span class="sxs-lookup"><span data-stu-id="08be5-101"><<<<<<< HEAD title: Filter and RecordCount Properties Example (VJ++) TOCTitle: Filter and RecordCount Properties Example (VJ++) ======= title: Filter and RecordCount properties example (VJ++) TOCTitle: Filter and RecordCount properties example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="08be5-102">главные ms:assetid: cf062f99-f935-6bf3-a245-fa345ead78db ms:mtpsurl: https://msdn.microsoft.com/library/JJ250025(v=office.15) ms:contentKeyID: 48547798 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="08be5-102">master ms:assetid: cf062f99-f935-6bf3-a245-fa345ead78db ms:mtpsurl: https://msdn.microsoft.com/library/JJ250025(v=office.15) ms:contentKeyID: 48547798 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="08be5-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="08be5-103"><<<<<<< HEAD</span></span>
# <a name="filter-and-recordcount-properties-example-vj"></a><span data-ttu-id="08be5-104">Filter and RecordCount Properties Example (VJ++)</span><span class="sxs-lookup"><span data-stu-id="08be5-104">Filter and RecordCount Properties Example (VJ++)</span></span>
=======
# <a name="filter-and-recordcount-properties-example-vj"></a><span data-ttu-id="08be5-105">Пример: свойства фильтра и RecordCount (VJ ++)</span><span class="sxs-lookup"><span data-stu-id="08be5-105">Filter and RecordCount properties example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="08be5-106">master</span><span class="sxs-lookup"><span data-stu-id="08be5-106">master</span></span>


<span data-ttu-id="08be5-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="08be5-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="08be5-108">В этом примере используется свойство [фильтра](filter-property-ado.md) для открытия нового [набора записей](recordset-object-ado.md) на основе указанного условия, применяемые к существующей **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="08be5-108">This example uses the [Filter](filter-property-ado.md) property to open a new [Recordset](recordset-object-ado.md) based on a specified condition applied to an existing **Recordset**.</span></span> <span data-ttu-id="08be5-109">Свойство [RecordCount](recordcount-property-ado.md) используется для отображения количества записей в двух **наборов записей**.</span><span class="sxs-lookup"><span data-stu-id="08be5-109">It uses the [RecordCount](recordcount-property-ado.md) property to show the number of records in the two **Recordsets**.</span></span> <span data-ttu-id="08be5-110">Функция FilterField является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="08be5-110">The FilterField function is required for this procedure to run.</span></span>

```java 
 
// BeginFilterJ 
// The WFC class includes the ADO objects. 
 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class FilterX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 FilterX(); 
 FilterX2(); 
 System.exit(0); 
 } 
 
 // FilterX function 
 static void FilterX() 
 { 
 
 // Define ADO Objects. 
 Recordset rstPublishers = null; 
 Recordset rstPublishersCountry = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String line = null; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 int intPublisherCount; 
 String strCountry; 
 String strMessage; 
 
 try 
 { 
 rstPublishers = new Recordset(); 
 
 // Open recordset with data from Publishers table. 
 rstPublishers.setCursorType(AdoEnums.CursorType.STATIC); 
 rstPublishers.open("publishers", strCnn, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TABLE); 
 
 // Populate the Recordset. 
 intPublisherCount = rstPublishers.getRecordCount(); 
 
 // Get user input. 
 System.out.println("Enter a country to filter on:"); 
 strCountry = in.readLine().trim(); 
 
 if(!strCountry.equals("")) 
 { 
 // Open a filtered Recordset object. 
 rstPublishersCountry = 
 FilterField(rstPublishers, "Country", strCountry); 
 if(rstPublishersCountry.getRecordCount()==0) 
 System.out.println("\nNo publishers from that country."); 
 else 
 { 
 // Print number of records for the original 
 // Recordset object and the filtered Recordset 
 // object. 
 strMessage = "\nOrders in original recordset: " + "\n" 
 + intPublisherCount + "\n" 
 + "Orders in filtered recordset (Country = '" 
 + strCountry + "'): \n" 
 + rstPublishersCountry.getRecordCount(); 
 System.out.println(strMessage); 
 } 
 rstPublishersCountry.close(); 
 } 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstPublishers != null) 
 { 
 PrintProviderError(rstPublishers.getActiveConnection()); 
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
 if (rstPublishers != null) 
 if (rstPublishers.getState() == 1) 
 rstPublishers.close(); 
 } 
 
 } 
 
 // FilterField Function 
 
 static Recordset FilterField(Recordset rstTemp,String strField, 
 String strFilter) 
 { 
 // Set a filter on the specified Recordset object and then 
 // open a new Recordset object. 
 rstTemp.setFilter(strField + " = '" + strFilter + "'"); 
 return rstTemp; 
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
 
 // FilterX2 function 
 
 static void FilterX2() 
 { 
 
 // Define ADO Objects. 
 Recordset rstPublishers = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String line = null; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 try 
 { 
 rstPublishers = new Recordset(); 
 
 // Open recordset with data from Publishers table. 
 rstPublishers.setCursorType(AdoEnums.CursorType.STATIC); 
 rstPublishers.open("SELECT * FROM publishers " + 
 "WHERE Country = 'USA'", strCnn, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TEXT); 
 
 // Print current data in recordset. 
 rstPublishers.moveFirst(); 
 while(!rstPublishers.getEOF()) 
 { 
 System.out.println(rstPublishers.getField("pub_name").getString() 
 +", " 
 + rstPublishers.getField("country").getString()); 
 rstPublishers.moveNext(); 
 } 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 // Cleanup objects before exit. 
 rstPublishers.close(); 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // Check for null pointer for connection object. 
 if (rstPublishers.getActiveConnection()==null) 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 else 
 { 
 // As passing a Recordset, check for null pointer first. 
 if (rstPublishers != null) 
 { 
 PrintProviderError(rstPublishers.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 } 
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 } 
} 
// EndFilterJ 
```

