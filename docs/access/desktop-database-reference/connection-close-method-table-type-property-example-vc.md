---
<span data-ttu-id="2f944-101"><<<<<<< Название HEAD: метод Close подключения, пример свойства типа таблица (VC ++) TOCTitle: метод Close подключения, пример свойства типа таблица (VC ++) === название: метод Close подключения, пример свойства типа таблица (VC ++) TOCTitle: Метод Close подключения, пример свойства типа таблица (VC ++)</span><span class="sxs-lookup"><span data-stu-id="2f944-101"><<<<<<< HEAD title: Connection Close Method, Table Type Property Example (VC++) TOCTitle: Connection Close Method, Table Type Property Example (VC++) ======= title: Connection Close Method, Table Type property example (VC++) TOCTitle: Connection Close Method, Table Type property example (VC++)</span></span>
>>>>>>> <span data-ttu-id="2f944-102">главные ms:assetid: d75fac58-4b25-c446-8c8e-4afcf1efecc5 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250082(v=office.15) ms:contentKeyID: 48548006 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="2f944-102">master ms:assetid: d75fac58-4b25-c446-8c8e-4afcf1efecc5 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250082(v=office.15) ms:contentKeyID: 48548006 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="2f944-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="2f944-103"><<<<<<< HEAD</span></span>
# <a name="connection-close-method-table-type-property-example-vc"></a><span data-ttu-id="2f944-104">Connection Close Method, Table Type Property Example (VC++)</span><span class="sxs-lookup"><span data-stu-id="2f944-104">Connection Close Method, Table Type Property Example (VC++)</span></span>
=======
# <a name="connection-close-method-table-type-property-example-vc"></a><span data-ttu-id="2f944-105">Метод Close подключения, пример свойства типа таблица (VC ++)</span><span class="sxs-lookup"><span data-stu-id="2f944-105">Connection Close Method, Table Type property example (VC++)</span></span>
>>>>>>> <span data-ttu-id="2f944-106">master</span><span class="sxs-lookup"><span data-stu-id="2f944-106">master</span></span>


<span data-ttu-id="2f944-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f944-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2f944-108">Для свойства [ActiveConnection](activeconnection-property-adox.md) значение **Nothing** «закрыть» каталог.</span><span class="sxs-lookup"><span data-stu-id="2f944-108">Setting the [ActiveConnection](activeconnection-property-adox.md) property to **Nothing** should "close" the catalog.</span></span> <span data-ttu-id="2f944-109">Связанные коллекции будет пустым.</span><span class="sxs-lookup"><span data-stu-id="2f944-109">Associated collections will be empty.</span></span> <span data-ttu-id="2f944-110">Любые объекты, которые были созданы на основе схемы объектам в каталоге будут изолированы.</span><span class="sxs-lookup"><span data-stu-id="2f944-110">Any objects that were created from schema objects in the catalog will be orphaned.</span></span> <span data-ttu-id="2f944-111">Любые свойства на те объекты, которые были кэшированы по-прежнему доступны, но при чтении свойства, которые требуют вызова к поставщику завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="2f944-111">Any properties on those objects that have been cached will still be available, but attempting to read properties that require a call to the provider will fail.</span></span>

```cpp 
 
// BeginCloseConnectionCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
#import "c:\Program Files\Common Files\system\ado\msado15.dll" 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void CloseConnectionByNothingX(void); 
void CloseConnectionX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 CloseConnectionByNothingX(); 
 CloseConnectionX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// CloseConnectionByNothingX Function // 
// // 
////////////////////////////////////////////////////////// 
void CloseConnectionByNothingX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 
 _CatalogPtr m_pCatalog = NULL; 
 _TablePtr m_pTable = NULL; 
 
 //Define ADODB object pointers 
 ADODB::_ConnectionPtr m_pCnn = NULL; 
 
 //Define other variables 
 _variant_t vIndex = (short) 0; 
 
 try 
 { 
 TESTHR(hr = m_pCnn.CreateInstance(__uuidof(ADODB::Connection))); 
 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof(Catalog))); 
 
 m_pCnn->Open("Provider='Microsoft.JET.OLEDB.4.0';" 
 "Data Source= 'c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';","","",NULL); 
 
 m_pCatalog->PutActiveConnection(_variant_t((IDispatch *)m_pCnn)); 
 
 m_pTable = m_pCatalog->Tables->GetItem(vIndex); 
 
 // Cache m_pTable.Type info 
 cout << m_pTable->Type << endl; 
 
 _variant_t vCnn; 
 vCnn.vt = VT_DISPATCH; 
 vCnn.pdispVal = NULL; 
 m_pCatalog->PutActiveConnection(vCnn); 
 
 // m_pTable is orphaned 
 cout << m_pTable->Type << endl; 
 // Previous line will succeed if this was cached 
 
 cout << m_pTable->Columns->GetItem(vIndex)->DefinedSize << endl; 
 // Previous line will fail if this info has not been cached 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 printf("\nError\n\tSource : %s \n\tdescription : %s \n", 
 (LPCSTR)bstrSource,(LPCSTR)bstrDescription); 
 } 
 catch(...) 
 { 
 cout << "Error occured in CloseConnectionByNothingX...."<< endl; 
 } 
} 
 
////////////////////////////////////////////////////////// 
// // 
// CloseConnectionX Function // 
// // 
////////////////////////////////////////////////////////// 
void CloseConnectionX() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 
 _CatalogPtr m_pCatalog = NULL; 
 _TablePtr m_pTable = NULL; 
 
 //Define ADODB object pointers 
 ADODB::_ConnectionPtr m_pCnn = NULL; 
 
 //Define other variables 
 _variant_t vIndex = (short) 0; 
 try 
 { 
 TESTHR(hr = m_pCnn.CreateInstance(__uuidof(ADODB::Connection))); 
 m_pCnn->Open("Provider='Microsoft.JET.OLEDB.4.0';" 
 "Data Source= 'c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';","","",NULL); 
 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof(Catalog))); 
 m_pCatalog->PutActiveConnection(_variant_t((IDispatch *)m_pCnn)); 
 
 m_pTable = m_pCatalog->Tables->GetItem(vIndex); 
 
 // Cache m_pTable.Type info 
 cout << m_pTable->Type << endl; 
 
 m_pCnn->Close(); 
 
 // m_pTable is orphaned 
 cout << m_pTable->Type << endl; 
 // Previous line will succeed if this was cached 
 
 cout << m_pTable->Columns->GetItem(vIndex)->DefinedSize << endl; 
 // Previous line will fail if this info has not been cached 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 printf("\nError\n\tSource : %s \n\tdescription : %s \n", 
 (LPCSTR)bstrSource,(LPCSTR)bstrDescription); 
 } 
 catch(...) 
 { 
 cout << "Error occured in CloseConnectionX...."<< endl; 
 } 
} 
// EndCloseConnectionCpp 
```

