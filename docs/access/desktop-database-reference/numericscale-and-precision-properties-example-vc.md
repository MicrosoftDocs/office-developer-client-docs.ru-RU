---
<span data-ttu-id="ed246-101"><<<<<<< Название HEAD: NumericScale и TOCTitle пример свойств точности (VC ++): NumericScale и пример: свойства точности (VC ++) === название: пример: свойства NumericScale и точность (VC ++) TOCTitle: NumericScale и Пример: свойства точности (VC ++)</span><span class="sxs-lookup"><span data-stu-id="ed246-101"><<<<<<< HEAD title: NumericScale and Precision Properties Example (VC++) TOCTitle: NumericScale and Precision Properties Example (VC++) ======= title: NumericScale and Precision properties example (VC++) TOCTitle: NumericScale and Precision properties example (VC++)</span></span>
>>>>>>> <span data-ttu-id="ed246-102">главные ms:assetid: da4bec90-b039-1764-3b8b-c74bb725da61 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250098(v=office.15) ms:contentKeyID: 48548078 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="ed246-102">master ms:assetid: da4bec90-b039-1764-3b8b-c74bb725da61 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250098(v=office.15) ms:contentKeyID: 48548078 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="ed246-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ed246-103"><<<<<<< HEAD</span></span>
# <a name="numericscale-and-precision-properties-example-vc"></a><span data-ttu-id="ed246-104">NumericScale and Precision Properties Example (VC++)</span><span class="sxs-lookup"><span data-stu-id="ed246-104">NumericScale and Precision Properties Example (VC++)</span></span>
=======
# <a name="numericscale-and-precision-properties-example-vc"></a><span data-ttu-id="ed246-105">Пример: свойства NumericScale и точность (VC ++)</span><span class="sxs-lookup"><span data-stu-id="ed246-105">NumericScale and Precision properties example (VC++)</span></span>
>>>>>>> <span data-ttu-id="ed246-106">master</span><span class="sxs-lookup"><span data-stu-id="ed246-106">master</span></span>


<span data-ttu-id="ed246-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed246-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ed246-108">В этом примере показано [NumericScale](numericscale-property-adox.md) и [точность](precision-property-adox.md) свойства объекта [столбца](column-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="ed246-108">This example demonstrates the [NumericScale](numericscale-property-adox.md) and [Precision](precision-property-adox.md) properties of the [Column](column-object-adox.md) object.</span></span> <span data-ttu-id="ed246-109">Этот код отображает значения для таблицы **Сведения о заказе** из базы данных *Northwind* .</span><span class="sxs-lookup"><span data-stu-id="ed246-109">This code displays their value for the **Order Details** table of the *Northwind* database.</span></span>

```cpp 
 
// BeginNumericScalePrecCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
#import "c:\Program Files\Common Files\system\ado\msado15.dll" 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void NumericScalePrecX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 NumericScalePrecX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// NumericScalePrecX Function // 
// // 
////////////////////////////////////////////////////////// 
void NumericScalePrecX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 _TablePtr m_pTable = NULL; 
 _ColumnPtr m_pColumn = NULL; 
 
 //Define ADODB object pointers 
 ADODB::_ConnectionPtr m_pCnn = NULL; 
 
 //Declare string variables 
 _bstr_t strCnn("Provider='Microsoft.JET.OLEDB.4.0';" 
 "Data Source='c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';"); 
 try 
 { 
 TESTHR(hr = m_pCnn.CreateInstance(__uuidof(ADODB::Connection))); 
 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof (Catalog))); 
 
 // Connect the catalog. 
 m_pCnn->Open (strCnn, "", "", NULL); 
 
 m_pCatalog->PutActiveConnection(variant_t((IDispatch *)m_pCnn)); 
 
 // Retrieve the Order Details table 
 m_pTable = m_pCatalog->Tables->GetItem("Order Details"); 
 
 // Display numeric scale and precision of 
 // small integer fields. 
 _variant_t vIndex; 
 for (long lIndex=0; lIndex < m_pTable->Columns->Count; lIndex++) 
 { 
 vIndex = lIndex ; 
 m_pColumn = m_pTable->Columns->GetItem(vIndex); 
 if(m_pColumn->Type == adSmallInt) 
 { 
 cout << "Column: " << m_pColumn->GetName() << endl; 
 cout << "Numeric scale: " << (_bstr_t) m_pColumn-> 
 GetNumericScale() << endl; 
 cout << "Precision: " << m_pColumn->GetPrecision() << 
 endl; 
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
 cout << "Error occured in NumericScalePrecX...."<< endl; 
 } 
} 
// EndNumericScalePrecCpp 
```

