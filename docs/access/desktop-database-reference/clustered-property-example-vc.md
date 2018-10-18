---
<span data-ttu-id="6a3b8-101"><<<<<<< Название HEAD: кластерные пример свойства (VC ++) TOCTitle: кластерные пример свойства (VC ++) === название: пример кластерные свойства (VC ++) TOCTitle: пример кластерные свойства (VC ++)</span><span class="sxs-lookup"><span data-stu-id="6a3b8-101"><<<<<<< HEAD title: Clustered Property Example (VC++) TOCTitle: Clustered Property Example (VC++) ======= title: Clustered property example (VC++) TOCTitle: Clustered property example (VC++)</span></span>
>>>>>>> <span data-ttu-id="6a3b8-102">главные ms:assetid: a262e38e-ce44-66cb-1adf-fad8e6b840d1 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249748(v=office.15) ms:contentKeyID: 48546761 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="6a3b8-102">master ms:assetid: a262e38e-ce44-66cb-1adf-fad8e6b840d1 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249748(v=office.15) ms:contentKeyID: 48546761 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="6a3b8-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6a3b8-103"><<<<<<< HEAD</span></span>
# <a name="clustered-property-example-vc"></a><span data-ttu-id="6a3b8-104">Clustered Property Example (VC++)</span><span class="sxs-lookup"><span data-stu-id="6a3b8-104">Clustered Property Example (VC++)</span></span>
=======
# <a name="clustered-property-example-vc"></a><span data-ttu-id="6a3b8-105">Пример свойства кластерные (VC ++)</span><span class="sxs-lookup"><span data-stu-id="6a3b8-105">Clustered property example (VC++)</span></span>
>>>>>>> <span data-ttu-id="6a3b8-106">master</span><span class="sxs-lookup"><span data-stu-id="6a3b8-106">master</span></span>


<span data-ttu-id="6a3b8-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a3b8-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6a3b8-108">В этом примере демонстрируется свойство [Clustered](clustered-property-adox.md) [индекса](index-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="6a3b8-108">This example demonstrates the [Clustered](clustered-property-adox.md) property of an [Index](index-object-adox.md).</span></span> <span data-ttu-id="6a3b8-109">Обратите внимание, что баз данных Microsoft Jet не поддерживают кластеризованных индексов, поэтому этот пример возвращает **значение False** для свойства **Clustered** всех индексов в базе *данных "Борей"* .</span><span class="sxs-lookup"><span data-stu-id="6a3b8-109">Note that Microsoft Jet databases do not support clustered indexes, so this example will return **False** for the **Clustered** property of all indexes in the *Northwind* database.</span></span>

```cpp 
 
// BeginClusteredCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void ClusteredX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 ClusteredX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// ClusteredX Function // 
// // 
////////////////////////////////////////////////////////// 
void ClusteredX() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 _TablePtr m_pTable = NULL; 
 _IndexPtr m_pIndex = NULL; 
 
 //Define other variables here 
 _variant_t vIndex; 
 try 
 { 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof(Catalog))); 
 
 // Connect to the catalog. 
 m_pCatalog->PutActiveConnection( 
 "Provider='Microsoft.JET.OLEDB.4.0';data source=" 
 "'c:\\Program Files\\Microsoft Office\\Office\\Samples" 
 "\\Northwind.mdb';"); 
 
 int iLineCnt = 1; 
 //Enumerate Tables. 
 for(short iTable = 0;iTable < m_pCatalog->Tables->Count;iTable++) 
 { 
 vIndex = iTable; 
 m_pTable = m_pCatalog->Tables->GetItem(vIndex); 
 
 //Enumerate Indexes. 
 for(short iIndex = 0;iIndex < m_pTable->Indexes->Count; 
 iIndex++) 
 { 
 vIndex = iIndex; 
 m_pIndex = m_pTable->Indexes->GetItem(vIndex); 
 cout << m_pTable->Name << " " ; 
 cout << m_pIndex->Name << " " << (m_pIndex-> 
 GetClustered() ? "True" : "False") << endl; 
 
 if (iLineCnt%15 == 0) 
 { 
 printf("\nPress any key to continue...\n"); 
 getch(); 
 } 
 iLineCnt++; 
 } 
 } 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 printf("\n\tSource : %s \n\tdescription : %s \n ", 
 (LPCSTR)bstrSource,(LPCSTR)bstrDescription); 
 } 
 catch(...) 
 { 
 cout << "Error occured in ClusteredX...."<< endl; 
 } 
} 
// EndClusteredCpp 
```

