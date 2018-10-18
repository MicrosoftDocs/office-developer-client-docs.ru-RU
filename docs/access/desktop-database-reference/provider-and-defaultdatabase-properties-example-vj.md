---
<span data-ttu-id="3d19f-101"><<<<<<< Название HEAD: поставщик и TOCTitle пример свойств DefaultDatabase (VJ ++): поставщика и пример: свойства DefaultDatabase (VJ ++) === заголовок: свойства пример поставщика и DefaultDatabase (VJ ++) TOCTitle: поставщика Пример свойства DefaultDatabase (VJ ++) и</span><span class="sxs-lookup"><span data-stu-id="3d19f-101"><<<<<<< HEAD title: Provider and DefaultDatabase Properties Example (VJ++) TOCTitle: Provider and DefaultDatabase Properties Example (VJ++) ======= title: Provider and DefaultDatabase properties example (VJ++) TOCTitle: Provider and DefaultDatabase properties example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="3d19f-102">главные ms:assetid: babd3c3c-bb6e-46ce-88f2-ef2810d798fd ms:mtpsurl: https://msdn.microsoft.com/library/JJ249898(v=office.15) ms:contentKeyID: 48547380 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="3d19f-102">master ms:assetid: babd3c3c-bb6e-46ce-88f2-ef2810d798fd ms:mtpsurl: https://msdn.microsoft.com/library/JJ249898(v=office.15) ms:contentKeyID: 48547380 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="3d19f-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="3d19f-103"><<<<<<< HEAD</span></span>
# <a name="provider-and-defaultdatabase-properties-example-vj"></a><span data-ttu-id="3d19f-104">Provider and DefaultDatabase Properties Example (VJ++)</span><span class="sxs-lookup"><span data-stu-id="3d19f-104">Provider and DefaultDatabase Properties Example (VJ++)</span></span>
=======
# <a name="provider-and-defaultdatabase-properties-example-vj"></a><span data-ttu-id="3d19f-105">Пример: свойства поставщика и DefaultDatabase (VJ ++)</span><span class="sxs-lookup"><span data-stu-id="3d19f-105">Provider and DefaultDatabase properties example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="3d19f-106">master</span><span class="sxs-lookup"><span data-stu-id="3d19f-106">master</span></span>


<span data-ttu-id="3d19f-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d19f-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3d19f-108">В этом примере демонстрируется свойство [поставщика](provider-property-ado.md) , открыв три объекты [подключения](connection-object-ado.md) , с помощью различных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="3d19f-108">This example demonstrates the [Provider](provider-property-ado.md) property by opening three [Connection](connection-object-ado.md) objects using different providers.</span></span> <span data-ttu-id="3d19f-109">Настройка базы данных по умолчанию для поставщика ODBC Microsoft также использует свойство [DefaultDatabase](defaultdatabase-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3d19f-109">It also uses the [DefaultDatabase](defaultdatabase-property-ado.md) property to set the default database for the Microsoft ODBC Provider.</span></span>

```java 
 
// BeginProviderJ 
import java.io.*; 
import com.ms.wfc.data.*; 
 
public class ProviderX 
{ 
 // The main entry point of the application. 
 public static void main (String[] args) 
 { 
 ProviderX(); 
 System.exit(0); 
 } 
 // ProviderX Function 
 static void ProviderX() 
 { 
 // Define ADO Objects. 
 Connection cnn1 = null; 
 Connection cnn2 = null; 
 Connection cnn3 = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader(new InputStreamReader(System.in)); 
 try 
 { 
 // Open a connection using the Microsoft ODBC Provider. 
 cnn1 = new Connection(); 
 cnn1.setConnectionString("driver={SQL Server};"+ 
 "server='MySqlServer';User ID='MyUserID';Password='MyPassword';"); 
 cnn1.open(); 
 cnn1.setDefaultDatabase("Pubs"); 
 
 // Display the provider. 
 System.out.println("\n\n\tCnn1 provider: "+ cnn1.getProvider()); 
 
 // Open connection using the OLE DB Provider for Microsoft Jet. 
 cnn2 = new Connection(); 
 cnn2.setProvider("Microsoft.Jet.OLEDB.4.0"); 
 cnn2.open("C:\\Program Files\\Microsoft Office\\Office\\Samples\\Northwind.mdb","admin",""); 
 
 // Display the provider. 
 System.out.println("\n\n\tCnn2 provider: " + 
 cnn2.getProvider()); 
 
 // Open a connection using the Microsoft SQL Server Provider. 
 cnn3 = new Connection(); 
 cnn3.setProvider("sqloledb"); 
 cnn3.open("Data Source='MySqlServer';Initial Catalog='Pubs';Integrated Security='SSPI';","",""); 
 
 // Display the provider. 
 System.out.println("\n\n\tCnn3 provider: " + 
 cnn3.getProvider()); 
 
 System.out.println("\n\n\tPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 catch(AdoException ae) 
 { 
 // Notify the user of any errors that result from ADO. 
 
 // As passing a Connection, check for null pointer first. 
 if(cnn1 != null) 
 { 
 PrintProviderError(cnn1); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getLocalizedMessage()); 
 } 
 } 
 // System read requires needs this catch. 
 catch(java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (cnn1 != null) 
 if (cnn1.getState() == 1) 
 cnn1.close(); 
 if (cnn2 != null) 
 if (cnn2.getState() == 1) 
 cnn2.close(); 
 if (cnn3 != null) 
 if (cnn3.getState() == 1) 
 cnn3.close(); 
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
// EndProviderJ 
```

