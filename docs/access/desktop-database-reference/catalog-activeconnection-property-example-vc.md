---
title: Catalog ActiveConnection Property Example (VC++)
TOCTitle: Catalog ActiveConnection Property Example (VC++)
ms:assetid: 0e72ff1c-b894-a440-67cf-bba091e7cb8b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248861(v=office.15)
ms:contentKeyID: 48543246
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 30eea3d77121712b33881cad13d3445de1467c81
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480497"
---
# <a name="catalog-activeconnection-property-example-vc"></a><span data-ttu-id="eb0d1-102">Catalog ActiveConnection Property Example (VC++)</span><span class="sxs-lookup"><span data-stu-id="eb0d1-102">Catalog ActiveConnection Property Example (VC++)</span></span>


<span data-ttu-id="eb0d1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb0d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="eb0d1-104">Установка для свойства [ActiveConnection](activeconnection-property-adox.md) допустимый, откройте подключение «открывает» каталог.</span><span class="sxs-lookup"><span data-stu-id="eb0d1-104">Setting the [ActiveConnection](activeconnection-property-adox.md) property to a valid, open connection "opens" the catalog.</span></span> <span data-ttu-id="eb0d1-105">Открытие каталога можно приступить к объекты схемы, содержащиеся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="eb0d1-105">From an open catalog, you can access the schema objects contained within that catalog.</span></span>

```cpp 
 
// BeginActiveConnectionCpp 
#import "c:\Program Files\Common Files\system\ado\msado15.dll" 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void OpenConnectionX(void); 
void OpenConnectionWithStringX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 OpenConnectionX(); 
 
 OpenConnectionWithStringX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// OpenConnectionX Function // 
// // 
////////////////////////////////////////////////////////// 
void OpenConnectionX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 
 //Define ADODB object pointers 
 ADODB::_ConnectionPtr m_pCnn = NULL; 
 
 // Define string variables. 
 _bstr_t strcnn("Provider='Microsoft.JET.OLEDB.4.0';" 
 "Data source = 'c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';"); 
 
 try 
 { 
 TESTHR(hr = m_pCnn.CreateInstance(__uuidof(ADODB::Connection))); 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof (Catalog))); 
 m_pCnn->Open(strcnn,"","",NULL); 
 m_pCatalog->PutActiveConnection(_variant_t((IDispatch *) m_pCnn)); 
 _variant_t vIndex = (short) 0; 
 cout<<m_pCatalog->Tables->GetItem(vIndex)->Type<<endl; 
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
 cout << "Error occured in OpenConnectionX...."<< endl; 
 } 
 
 if (m_pCnn) 
 if (m_pCnn->State == 1) 
 m_pCnn->Close(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// OpenConnectionWithStringX Function // 
// // 
////////////////////////////////////////////////////////// 
void OpenConnectionWithStringX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 
 // Define string variables. 
 _bstr_t strcnn("Provider='Microsoft.JET.OLEDB.4.0';" 
 "Data source = 'c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';"); 
 
 try 
 { 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof (Catalog))); 
 m_pCatalog->PutActiveConnection(strcnn); 
 _variant_t vIndex = (short) 0; 
 cout<<m_pCatalog->Tables->GetItem(vIndex)->Type<<endl; 
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
 cout << "Error occured in OpenConnectionWithStringX...."<< endl; 
 } 
} 
// EndActiveConnectionCpp 
```

